---
title: Accès à un message dans une banque IMAP sans télécharger le message entier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 61e81b2b078718bdb7d11d3dc5f99e192077eaa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551449"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Accès à un message dans une banque IMAP sans télécharger le message entier

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente un exemple de code en C++ qui interroge une magasin de messages pour l’interface **[IProxyStoreObject](iproxystoreobject.md)** et utilise le pointeur renvoyé et la fonction **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** pour obtenir un pointeur vers un objet de magasin IMAP qui a été déballé. L’utilisation de cette magasine non ballée permet d’accéder à un message dans son état actuel sans appel d’un téléchargement de l’intégralité du message. 
  
Comme **UnwrapNoRef** n’incrémente pas le nombre de références pour ce nouveau pointeur vers l’objet store non enveloppé, après avoir correctement appelé **UnwrapNoRef,** vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) pour conserver le nombre de références. 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```


