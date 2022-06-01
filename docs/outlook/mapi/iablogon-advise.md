---
title: IABLogonAdvise
description: Cet article décrit la fonction IABLogonAdvise et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
ms.openlocfilehash: a637858ab3f3e034636612cf5270c381c758662a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815799"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit l’appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées.
    
 _ulEventMask_
  
> [in] Masque de bits des valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et doivent être inclus dans l’inscription. Une structure [NOTIFICATION](notification.md) correspondante est associée à chaque type d’événement qui contient des informations sur l’événement. Le tableau suivant répertorie les valeurs valides pour le paramètre  _ulEventMask_ et les structures associées à chaque valeur. 
    
|**Type d’événement de notification**|**Structure **notification** correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Pointeur vers un objet récepteur de conseil pour recevoir les notifications suivantes.
    
 _lpulConnection_
  
> [out] Pointeur vers une valeur différente de zéro qui représente l’inscription de notification.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L’identificateur d’entrée passé dans le paramètre _lpEntryID_ n’est pas au format approprié. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d’adresses ne prend pas en charge la notification, peut-être parce qu’il n’autorise pas les modifications apportées à ses objets.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnet d’adresses ne peut pas gérer l’identificateur d’entrée passé dans  _lpEntryID_.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d’adresses implémentent la méthode **IABLogon::Advise** pour inscrire l’appelant afin d’être averti lorsqu’une modification est apportée à un objet dans l’un de ses conteneurs. Les appelants peuvent s’inscrire aux notifications concernant les utilisateurs de messagerie, les listes de distribution ou des conteneurs entiers. 
  
Les clients appellent généralement la méthode [IAddrBook::Advise](iaddrbook-advise.md) pour s’inscrire aux notifications de carnet d’adresses. MAPI appelle ensuite la méthode **Advise** du fournisseur de carnet d’adresses responsable de l’objet représenté par l’identificateur d’entrée dans  _lpEntryID_.
  
Lorsqu’une modification est apportée à l’objet indiqué du type représenté dans  _ulEventMask_, un appel est effectué à la méthode **OnNotify** du récepteur de conseils pointé par  _lpAdviseSink_. Les données transmises dans la structure **NOTIFICATION** à la routine **OnNotify** décrivent l’événement. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez gérer les notifications avec ou sans l’aide de MAPI. MAPI dispose de trois méthodes d’objet de prise en charge pour aider les fournisseurs de services à implémenter la notification :
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si vous choisissez d’utiliser les méthodes de support MAPI, appelez **Subscribe** lorsque votre méthode **Advise** est appelée et relâchez le pointeur  _lpAdviseSink_ . 
  
Si vous choisissez de prendre en charge la notification vous-même, appelez la méthode **AddRef** du récepteur de conseils représenté par le paramètre  _lpAdviseSink_ pour conserver une copie de ce pointeur. Conservez cette copie jusqu’à ce que votre méthode [IABLogon::Unadvise](iablogon-unadvise.md) soit appelée pour annuler l’inscription. 
  
Quelle que soit la façon dont vous prenez en charge la notification, attribuez un numéro de connexion différent de zéro à l’inscription de notification et retournez-le dans le paramètre _lpulConnection_ . Ne relâchez pas ce numéro de connexion tant que la méthode **Unadvise** n’a pas été appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le pointeur récepteur conseiller que vous passez dans le paramètre _lpAdviseSink_ à **Conseiller** peut pointer vers un objet que vous avez créé ou que MAPI a créé via la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . Vous pouvez utiliser **HrThisThreadAdviseSink** si vous prenez en charge plusieurs threads d’exécution et que vous souhaitez être sûr que les appels suivants à votre méthode **OnNotify** se produisent à un moment approprié sur un thread approprié. 
  
Préparez-vous à ce que l’objet récepteur de votre avis soit libéré à tout moment après votre appel à **Conseiller** et avant votre appel à **Unadvise**. Par conséquent, vous devez libérer votre objet récepteur de conseils après le retour de **Conseiller** , sauf si vous avez une utilisation à long terme spécifique pour celui-ci. 
  
Pour plus d’informations sur le processus de notification, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez [Notification d’événement de prise en charge](supporting-event-notification.md). Pour plus d’informations sur le multithreading et MAPI, consultez [Threading dans MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

