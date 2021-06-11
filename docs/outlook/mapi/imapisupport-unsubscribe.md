---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421213"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule la responsabilité de l’envoi de notifications précédemment établies avec un appel à la méthode [IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Numéro de connexion autre que zéro qui représente l’inscription de notification précédemment établie via **IMAPISupport::Subscribe**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification a été annulée.
    
MAPI_E_NOT_FOUND 
  
> Le numéro de connexion transmis dans le  _paramètre ulConnection_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::Unsubscribe** est implémentée pour tous les objets de support du fournisseur de services. Les fournisseurs de services **appellent Unsubscribe** pour annuler une inscription de notification précédemment définie par **Subscribe**. **L’annulation de l’abonnement** annule l’inscription en libérant le pointeur de sink de conseil transmis dans **l’appel d’abonnement.** 
  
En règle générale, la méthode **IUnknown::Release** du sink de conseil est appelée pendant l’appel **de désabonnement.** Toutefois, si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de sink de conseil, l’appel de publication est retardé jusqu’à ce que la méthode **OnNotify** renvoie.  
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

