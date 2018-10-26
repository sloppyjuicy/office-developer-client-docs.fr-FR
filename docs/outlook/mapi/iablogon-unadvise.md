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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3fbf8b423cfd4206a0143b5639c85dbcacce2fae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570981"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule les notifications qui ont été précédemment configurées avec un appel à la méthode [IABLogon::Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Le numéro de connexion associé à un enregistrement de notification actif. Un appel précédent à **Advise** doit renvoyer la valeur de la _classe ulConnection_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de notification a été annulée.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **Unadvise** pour annuler un enregistrement de notification pour un conteneur, utilisateur ou objet liste de distribution de messagerie. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Votre implémentation de **Unadvise** varient selon que vous prenez en charge la notification manuellement ou à l’aide de MAPI. Si MAPI propose votre prise en charge, appelez la méthode [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) pour annuler l’inscription. Si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, elle peut être retardée jusqu'à ce que **OnNotify** a renvoyé. 
  
Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md). Pour plus d’informations sur l’utilisation de la [IMAPISupport : IUnknown](imapisupportiunknown.md) méthodes pour prendre en charge la notification, consultez [Prise en charge de Notification d’événement](supporting-event-notification.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

