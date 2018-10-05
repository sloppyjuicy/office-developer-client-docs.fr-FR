---
title: Accéder à un message dans une banque IMAP sans télécharger l’intégralité du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398443"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Accéder à un message dans une banque IMAP sans télécharger l’intégralité du message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente un exemple de code en langage C++ qui interroge une banque de messages pour l’interface **[IProxyStoreObject](iproxystoreobject.md)** et utilise le pointeur retourné et la fonction **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** pour obtenir un pointeur vers un objet banque IMAP qui a été dévoilé. À l’aide de ce magasin non permet d’accéder à un message dans son état actuel sans appeler un téléchargement de l’intégralité du message. 
  
Car **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après l’appel à **UnwrapNoRef**avec succès, vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) pour maintenir le décompte de références. 
  
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


