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
ms.openlocfilehash: 01ea05eb864c78f3ded39ca3ebc62578076b9d37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584659"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule la responsabilité de l’envoi de notifications précédemment établie par un appel à la méthode [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Le numéro de connexion différente de zéro qui représente l’enregistrement de notification précédemment établie par le biais de **IMAPISupport::Subscribe**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de notification a été annulée.
    
MAPI_E_NOT_FOUND 
  
> Le numéro de connexion passé dans le paramètre _ulConnection_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::Unsubscribe** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services d’appel **désabonnement** pour annuler un enregistrement de notification précédemment configuré par **abonnement**. **Annuler l’abonnement** annule l’inscription en libérant le pointeur du récepteur advise passé dans l’appel de **s’abonner** . 
  
En règle générale, méthode de **IUnknown::Release** du récepteur advise est appelé pendant l’appel de **désabonnement** . Toutefois, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

