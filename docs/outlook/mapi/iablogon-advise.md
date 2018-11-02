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
ms.openlocfilehash: ea72a6fd2a22fe87ad63bb9c8fa6c1416d876b66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564247"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre l’appelant pour recevoir des notifications d’événements spécifiques qui affectent un conteneur, utilisateur ou liste de distribution de messagerie.
  
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
  
> [in] Le nombre d’octets de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées.
    
 _ulEventMask_
  
> [in] Un masque binaire composé des valeurs qui indiquent les types d’événements de notification que l’appelant est intéressée par et doit être inclus dans l’enregistrement. Il existe une structure [NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui conserve des informations sur l’événement. Le tableau suivant répertorie les valeurs valides pour le paramètre _ulEventMask_ et les structures associés à chaque valeur. 
    
|**Type d’événement notification**|**Structure **NOTIFICATION** correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures.
    
 _lpulConnection_
  
> [out] Pointeur vers une valeur différente de zéro qui représente l’enregistrement de notification.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L’identificateur d’entrée passé dans le paramètre _lpEntryID_ n’est pas au format approprié. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d’adresses ne gère pas la notification, éventuellement, car il n’autorise pas les modifications apportées à ses objets.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnet d’adresses ne peut pas gérer l’identificateur d’entrée passé _lpEntryID_.
    
## <a name="remarks"></a>Remarques

Fournisseurs de carnet d’adresses implémentent la méthode **IABLogon::Advise** pour enregistrer l’appelant à être averti lorsque cet événement se produit une modification à un objet dans un de leurs conteneurs. Les appelants peuvent s’inscrire pour les notifications concernant les utilisateurs de messagerie, des listes de distribution ou des conteneurs entières. 
  
Généralement, les clients appeler la méthode [IAddrBook::Advise](iaddrbook-advise.md) pour enregistrer les notifications de carnet d’adresse. MAPI appelle ensuite la méthode **Advise** du fournisseur de carnet d’adresses qui est responsable de l’objet représenté par l’identificateur d’entrée dans _lpEntryID_.
  
Lorsqu’une modification est apportée à l’objet du type représenté dans _ulEventMask_indiqué, un appel est effectué à la méthode **OnNotify** du récepteur advise désigné par _lpAdviseSink_. Données transmises dans la structure de **NOTIFICATION** à la routine **OnNotify** décrivent l’événement. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Vous pouvez prendre en charge notification avec ou sans l’aide de MAPI. MAPI a trois méthodes d’objet de prise en charge pour aider les fournisseurs de services à implémenter la notification :
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si vous choisissez d’utiliser les méthodes de prise en charge MAPI, appelé la méthode **Subscribe** lorsque votre méthode **Advise** est appelée et libérer le pointeur _lpAdviseSink_ . 
  
Si vous choisissez prendre en charge de notification vous-même, appeler la méthode **AddRef** du récepteur advise représenté par le paramètre _lpAdviseSink_ de conserver une copie de ce pointeur. Mettre à jour cette copie jusqu'à ce que votre méthode [IABLogon::Unadvise](iablogon-unadvise.md) est appelée pour annuler l’inscription. 
  
Quelle que soit la façon dont vous prenez en charge la notification, affecter un numéro de connexion différente de zéro pour l’inscription de notification et la faire revenir dans le paramètre _lpulConnection_ . Ne relâchez pas ce numéro de connexion jusqu'à ce que la méthode **Unadvise** a été appelée. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Le pointeur du récepteur advise que vous passez dans le paramètre _lpAdviseSink_ à **Advise** peut pointer vers un objet que vous avez créé ou MAPI créé par le biais de la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . Vous pouvez souhaiter utiliser **HrThisThreadAdviseSink** si vous prennent en charge plusieurs threads d’exécution et que vous voulez utiliser pour vous assurer que les appels suivants à votre méthode **OnNotify** se produire à un moment opportun sur une thread approprié. 
  
Être préparé pour être libéré à tout moment après votre appel **Advise** et avant l’appel de **Unadvise**votre objet récepteur advise. Par conséquent, vous devez libérer votre objet de récepteur advise après **Advise** renvoie, à moins d’avoir une utilisation à long terme spécifique pour qu’il. 
  
Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md). Pour plus d’informations sur la façon d’utiliser les méthodes **IMAPISupport** pour prendre en charge la notification, voir [Prise en charge de Notification d’événement](supporting-event-notification.md). Pour plus d’informations sur le multithreading et MAPI, consultez [Threading MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

