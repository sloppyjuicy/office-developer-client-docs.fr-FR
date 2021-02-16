---
title: Accès à un message dans une banque IMAP sans télécharger le message entier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299075"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Accès à un message dans une banque IMAP sans télécharger le message entier

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente un exemple de code en C++ qui interroge une magasin de messages pour l’interface **[IProxyStoreObject](iproxystoreobject.md)** et utilise le pointeur renvoyé et la fonction **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** pour obtenir un pointeur vers un objet de magasin IMAP qui a été déballé. L’utilisation de cette magasine non enveloppée permet d’accéder à un message dans son état actuel sans appel d’un téléchargement de l’intégralité du message. 
  
Étant donné que **UnwrapNoRef** n’incrémente pas le nombre de références pour ce nouveau pointeur vers l’objet store non enveloppé, après avoir correctement appelé **UnwrapNoRef,** vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) pour conserver le nombre de références. 
  
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


