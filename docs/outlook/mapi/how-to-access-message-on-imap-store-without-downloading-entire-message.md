---
title: Accéder à un message dans une banque IMAP sans télécharger l’intégralité du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fa7a61da47169ca7c6a1521ad5b3e84685a9b9a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783484"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Accéder à un message dans une banque IMAP sans télécharger l’intégralité du message

**S’applique à**: Outlook 
  
Cette rubrique présente un exemple de code en langage C++ qui interroge une banque de messages pour l’interface **[IProxyStoreObject](iproxystoreobject.md)** et utilise le pointeur retourné et la fonction **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** pour obtenir un pointeur vers un objet banque IMAP qui a été dévoilé. À l’aide de ce magasin non permet d’accéder à un message dans son état actuel sans appeler un téléchargement de l’intégralité du message. 
  
Car **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après l’appel à **UnwrapNoRef**avec succès, vous devez appeler [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) pour maintenir le décompte de références. 
  
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


