---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428227"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit l'appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet sur lequel les notifications doivent être générées.
    
 _ulEventMask_
  
> dans Masque de valeurs qui indique les types d'événements de notification qui intéressent l'appelant et qui doit être inclus dans l'inscription. Il existe une structure de [notification](notification.md) correspondante associée à chaque type d'événement qui contient des informations sur l'événement. Le tableau suivant répertorie les valeurs valides pour le paramètre _ulEventMask_ et les structures associées à chaque valeur. 
    
|**Type d'événement de notification**|**Structure de **notification** correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes.
    
 _lpulConnection_
  
> remarquer Pointeur vers une valeur différente de zéro qui représente l'enregistrement de la notification.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'enregistrement de la notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L'identificateur d'entrée passé dans le paramètre _lpEntryID_ n'est pas au format approprié. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d'adresses ne prend pas en charge la notification, probablement parce qu'il ne permet pas de modifier les objets.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnet d'adresses ne peut pas gérer l'identificateur d'entrée transmis dans _lpEntryID_.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d'adresses implémentent la méthode **IABLogon:: Advise** pour enregistrer l'appelant lorsqu'une modification est apportée à un objet dans l'un de ses conteneurs. Les appelants peuvent s'inscrire pour les notifications relatives aux utilisateurs de messagerie, aux listes de distribution ou aux conteneurs entiers. 
  
Les clients appellent généralement la méthode [IAddrBook:: Advise](iaddrbook-advise.md) pour s'inscrire aux notifications de carnet d'adresses. MAPI appelle ensuite la **** méthode Advise du fournisseur de carnet d'adresses qui est responsable de l'objet représenté par l'identificateur d'entrée dans _lpEntryID_.
  
Lorsqu'une modification est apportée à l'objet indiqué du type représenté dans _ulEventMask_, un appel est passé à la méthode **OnNotify** du récepteur conseillers vers lequel pointe _lpAdviseSink_. Les données transmises dans la structure de **notification** à la routine **OnNotify** décrivent l'événement. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez prendre en charge les notifications avec ou sans l'aide de MAPI. MAPI dispose de trois méthodes d'objet de prise en charge pour aider les fournisseurs de services à mettre en œuvre la notification:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si vous choisissez d'utiliser les méthodes de prise en charge MAPI, appelez **subscribe** lorsque votre méthode Advise est appelée et relâchez le pointeur _lpAdviseSink_ . **** 
  
Si vous choisissez de prendre en charge la notification vous-même, appelez la méthode **AddRef** du récepteur de notifications représenté par le paramètre _lpAdviseSink_ pour conserver une copie de ce pointeur. Conservez cette copie jusqu'à ce que la méthode [IABLogon::](iablogon-unadvise.md) Unadvise soit appelée pour annuler l'inscription. 
  
Quelle que soit la façon dont vous prenez en charge la notification, attribuez un numéro de connexion différent de zéro à l'enregistrement des notifications et renvoyez-le dans le paramètre _lpulConnection_ . Ne libérez pas ce numéro de connexion **** tant que la méthode Unadvise n'a pas été appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le pointeur de récepteur de notifications transmis dans le paramètre _lpAdviseSink_ à Advise peut pointer vers un objet que vous avez créé ou que MAPI a créé par le biais de la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . **** Vous pouvez utiliser **HrThisThreadAdviseSink** si vous prenez en charge plusieurs threads d'exécution et que vous souhaitez vous assurer que les appels suivants à votre méthode **OnNotify** se produisent à un moment approprié sur un thread approprié. 
  
Préparez-vous à ce que votre objet de récepteur de notifications soit libéré à tout moment après votre appel à **conseiller** et avant l'appel à Unadvise. **** Par conséquent, vous devez libérer votre objet de récepteur **** d'avertissement une fois qu'il a été renvoyé, sauf si vous disposez d'une utilisation de longue durée spécifique. 
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). Pour plus d'informations sur l'utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez la rubrique [prise en](supporting-event-notification.md)charge des notifications d'événements. Pour plus d'informations sur le multithreading et MAPI, voir [Threading in MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

