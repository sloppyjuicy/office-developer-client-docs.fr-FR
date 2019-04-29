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
  
Annule la responsabilité pour l'envoi de notifications précédemment établies avec un appel à la méthode [IMAPISupport:: subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> dans Numéro de connexion différent de zéro qui représente l'inscription de notification précédemment établie via **IMAPISupport:: subscribe**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'enregistrement de la notification a été annulé.
    
MAPI_E_NOT_FOUND 
  
> Le numéro de connexion transmis dans le paramètre _ulConnection_ n'existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: unsubscribe** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de **** services appellent unsubscribe pour annuler une inscription aux notifications précédemment configurée par **subscribe**. **Unsubscribe** annule l'inscription en publiant le pointeur de récepteur de notifications transmis à l'appel **subscribe** . 
  
En règle générale, la méthode **IUnknown:: Release** du récepteur de notification est appelée pendant l'appel de **désinscription** . Toutefois, si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet de récepteur de notifications, l'appel de **libération** est retardé jusqu'à ce que la méthode **OnNotify** soit renvoyée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

