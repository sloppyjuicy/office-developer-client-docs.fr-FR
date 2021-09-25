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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f1cfafc1236f2347527efd9022c4484dffee229
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614037"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule les notifications précédemment définies avec un appel à la [méthode IABLogon::Advise.](iablogon-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Numéro de connexion associé à un enregistrement de notification actif. Un appel précédent au **conseil** doit avoir renvoyé la valeur  _de ulConnection_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification a été annulée avec succès.
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode Unadvise** pour annuler l’inscription d’une notification pour un objet conteneur, utilisateur de messagerie ou liste de distribution. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Votre implémentation **d’Unadvise** dépend de la prise en charge de la notification avec l’aide de MAPI ou manuellement. Si MAPI fournit votre prise en charge, appelez la méthode [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) pour annuler l’inscription. Si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de conseil, il peut être retardé jusqu’à ce que **OnNotify** soit renvoyé. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur l’utilisation des méthodes [IMAPISupport : IUnknown](imapisupportiunknown.md) pour prendre en charge la notification, voir [Notification d’événement de prise en charge.](supporting-event-notification.md)
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

