---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348880"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule les notifications précédemment configurées avec un appel à la méthode [IABLogon:: Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> dans Numéro de connexion associé à l'enregistrement de notifications actif. Un appel précédent à **Advise** doit avoir renvoyé la valeur de _ulConnection_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'inscription de la notification a été annulée.
    
## <a name="remarks"></a>Remarques

MAPI appelle la **** méthode Unadvise pour annuler une inscription de notification pour un conteneur, un utilisateur de messagerie ou un objet de liste de distribution. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L'implémentation de **** Unadvise varie selon que vous prenez en charge la notification avec l'aide de MAPI ou manuellement. Si MAPI fournit votre prise en charge, appelez la méthode [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) pour annuler l'inscription. Si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification, il peut être retardé jusqu'à ce que **OnNotify** ait renvoyé. 
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). Pour plus d'informations sur l'utilisation des méthodes [IMAPISupport: IUnknown](imapisupportiunknown.md) pour prendre en charge la notification, consultez la rubrique [notification d'événement de prise en](supporting-event-notification.md)charge.
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

