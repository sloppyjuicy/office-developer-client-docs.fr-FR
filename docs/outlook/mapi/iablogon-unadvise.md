---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
ms.openlocfilehash: 0dcd82f4ebb5738bffa24a65c949174440a8ad7b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379177"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule les notifications précédemment définies avec un appel à la [méthode IABLogon::Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Numéro de connexion associé à un enregistrement de notification actif. Un appel précédent à **Advise** doit avoir renvoyé la valeur  _de ulConnection_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification a été annulée avec succès.
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode Unadvise** pour annuler l’inscription d’une notification pour un objet conteneur, utilisateur de messagerie ou liste de distribution. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Votre implémentation **d’Unadvise** dépend de la prise en charge de la notification avec l’aide de MAPI ou manuellement. Si MAPI fournit votre prise en charge, appelez la méthode [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) pour annuler l’inscription. Si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de conseil, il peut être retardé jusqu’à ce que **OnNotify** soit renvoyé. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur l’utilisation des méthodes [IMAPISupport : IUnknown](imapisupportiunknown.md) pour prendre en charge la notification, voir [Notification d’événement de prise en charge](supporting-event-notification.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

