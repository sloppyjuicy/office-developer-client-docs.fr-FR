---
title: IABLogonAdvise
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bae6730ea0ef8f0061c64f4da794b36d8ca8c226
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463830"
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées.
    
 _ulEventMask_
  
> [in] Masque de bits de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et qui doivent être inclus dans l’inscription. Il existe une structure [de NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui contient des informations sur l’événement. Le tableau suivant répertorie les valeurs valides pour le  _paramètre ulEventMask_ et les structures associées à chaque valeur. 
    
|**Type d’événement de notification**|**Structure **de NOTIFICATION** correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes.
    
 _lpulConnection_
  
> [out] Pointeur vers une valeur autre que zéro qui représente l’inscription de la notification.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L’identificateur d’entrée transmis _dans le paramètre lpEntryID_ n’est pas dans le format approprié. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d’adresses ne prend pas en charge la notification, éventuellement parce qu’il n’autorise pas les modifications apportées à ses objets.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnet d’adresses ne peut pas gérer l’identificateur d’entrée transmis  _dans lpEntryID_.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d’adresses implémentent la méthode **IABLogon::Advise** pour inscrire l’appelant afin qu’il soit averti lorsqu’une modification est appliquée à un objet dans l’un de ses conteneurs. Les appelants peuvent s’inscrire aux notifications concernant les utilisateurs de messagerie, les listes de distribution ou les conteneurs entiers. 
  
Les clients appellent généralement [la méthode IAddrBook::Advise](iaddrbook-advise.md) pour s’inscrire aux notifications de carnet d’adresses. MAPI appelle ensuite la méthode **Advise** du fournisseur de carnet d’adresses responsable de l’objet représenté par l’identificateur d’entrée  _dans lpEntryID_.
  
Lorsqu’une modification a lieu sur l’objet indiqué du type représenté dans  _ulEventMask_, un appel est effectué à la méthode **OnNotify** du sink de conseil pointé par  _lpAdviseSink_. Les données transmises dans **la structure NOTIFICATION** à **la routine OnNotify** décrivent l’événement. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez prendre en charge les notifications avec ou sans l’aide de MAPI. MAPI dispose de trois méthodes objet de support pour aider les fournisseurs de services à implémenter la notification :
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si vous utilisez les méthodes de support MAPI, appelez **Subscribe** lorsque votre méthode **Advise** est appelée et relâchez le pointeur  _lpAdviseSink_ . 
  
Si vous avez choisi de prendre en charge la notification vous-même, appelez la méthode **AddRef** du sink de notification représenté par le paramètre  _lpAdviseSink_ pour conserver une copie de ce pointeur. Conservez cette copie jusqu’à ce que votre [méthode IABLogon::Unadvise](iablogon-unadvise.md) soit appelée pour annuler l’inscription. 
  
Quelle que soit la prise en charge de la notification, affectez un numéro de connexion non zéro à l’inscription de la notification et renvoyez-le dans _le paramètre lpulConnection_ . Ne relâchez pas ce numéro de connexion tant que **la méthode Unadvise** n’a pas été appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le pointeur de sink de conseil que vous passez au paramètre _lpAdviseSink_ à **Advise** peut pointer vers un objet que vous avez créé ou que MAPI a créé via la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . Vous pouvez utiliser **HrThisThreadAdviseSink** si vous prisez en charge plusieurs threads d’exécution et que vous souhaitez vous assurer que les appels ultérieurs à votre méthode **OnNotify** se produisent à un moment approprié sur un thread approprié. 
  
Soyez prêt à ce que votre objet de sink de conseil soit libéré à tout moment après votre appel à **Advise** et avant votre appel à **Unadvise**. Par conséquent, vous devez libérer votre objet de sink de conseil après le retour de **Advise** , sauf si vous avez une utilisation spécifique à long terme pour lui. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Notification d’événement de prise en charge](supporting-event-notification.md). Pour plus d’informations sur le multithreading et MAPI, voir [Threading dans MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

