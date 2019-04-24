---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334754"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un client ou un fournisseur de services pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées du carnet d'adresses.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du conteneur de carnet d'adresses, de l'utilisateur de messagerie ou de la liste de distribution qui générera une notification lorsqu'une modification est apportée au type ou aux types décrits dans le paramètre _ulEventMask_ . 
    
 _ulEventMask_
  
> dans Un ou plusieurs événements de notification que l'appelant s'inscrit à recevoir. Chaque événement est associé à une structure de notification spécifique qui contient des informations sur la modification qui s'est produite. Le tableau suivant répertorie les valeurs valides pour _ulEventMask_ et leurs structures correspondantes. 
    
|**Notification, événement**|**Structure correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> dans Pointeur vers l'objet de récepteur de Conseil à appeler lorsque l'événement pour lequel la notification a été demandée se produit.
    
 _lpulConnection_
  
> remarquer Pointeur vers un numéro de connexion différent de zéro qui représente l'enregistrement de la notification.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'enregistrement de la notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> Le fournisseur de carnet d'adresses responsable de l'identificateur d'entrée passé dans _lpEntryID_ n'a pas pu enregistrer une notification pour l'entrée correspondante. 
    
MAPI_E_NO_SUPPORT 
  
> La notification n'est pas prise en charge par le fournisseur de carnet d'adresses responsable de l'objet identifié par l'identificateur d'entrée passé dans le paramètre _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'identificateur d'entrée passé dans _lpEntryID_ ne peut être géré par aucun des fournisseurs de carnet d'adresses dans le profil. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de **** services appellent la méthode Advise pour s'inscrire à un type particulier ou à des types de notifications sur une entrée de carnet d'adresses. Les types de notifications sont indiqués par le masque d'événement transmis avec le paramètre _ulEventMask_ . 
  
MAPI transmet cet appel **** au fournisseur de carnets d'adresses qui est responsable de l'entrée comme indiqué par l'identificateur d'entrée dans le paramètre _lpEntryID_ . Le fournisseur de carnet d'adresses gère l'inscription proprement dite ou appelle la méthode de prise en charge, [IMAPISupport:: subscribe](imapisupport-subscribe.md), pour inviter MAPI à inscrire l'appelant. Un numéro de connexion différent de zéro est renvoyé pour représenter la réussite de l'inscription.
  
Chaque fois qu'une modification est apportée à l'entrée du type indiqué par l'enregistrement des notifications, le fournisseur de carnet d'adresses appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet récepteur de notification spécifié dans le paramètre _lpAdviseSink_ . La méthode **OnNotify** inclut une structure de [notification](notification.md) sous la forme d'un paramètre d'entrée qui contient les données de description de l'événement. 
  
En fonction du fournisseur de carnet d'adresses, l'appel à **OnNotify** peut se produire immédiatement après la modification de l'objet inscrit ou ultérieurement. Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut se produire sur n'importe quel thread. Les clients peuvent demander que ces notifications se produisent sur un thread particulier en appelant la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer l'objet de récepteur de notifications qui est transmis à Advise. **** 
  
Étant donné qu'un fournisseur de carnet d'adresses peut libérer l'objet de récepteur de notifications transmis par les clients à tout **** moment après l'exécution réussie de l'appel de la méthode Advise et avant un appel [IAddrBook::](iaddrbook-unadvise.md) Unadvise pour annuler la notification, les clients doivent le libérer. leurs objets de récepteur de **** notification lorsque la fonction Advise renvoie. 
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

