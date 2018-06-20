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
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783620"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**S’applique à**: Outlook 
  
Enregistre un fournisseur de service ou client pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses, messagerie utilisateur ou liste de distribution qui générera une notification en cas de modification du type ou de types décrits dans le paramètre _ulEventMask_ . 
    
 _ulEventMask_
  
> [in] Un ou plusieurs événements de notification qui inscrit pour la réception de l’appelant. Chaque événement est associé à une structure de notification spécifique qui contient des informations sur les modifications apportées. Le tableau suivant répertorie les valeurs valides pour _ulEventMask_ et leurs structures correspondantes. 
    
|**Événement de notification**|**Structure correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Pointeur vers l’objet de récepteur advise à appeler lorsque l’événement pour lequel la notification a été demandée.
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro de connexion différente de zéro qui représente l’enregistrement de notification.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’inscription de notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> Le fournisseur de carnet d’adresses responsable de l’identificateur d’entrée passé _lpEntryID_ n’a pas pu enregistrer une notification de l’entrée correspondante. 
    
MAPI_E_NO_SUPPORT 
  
> Notification n’est pas pris en charge par le fournisseur de carnet d’adresses responsable de l’objet identifié par l’identificateur d’entrée passé dans le paramètre _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée passé _lpEntryID_ ne peuvent pas être géré par des fournisseurs du carnet d’adresses dans le profil. 
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **Advise** pour inscrire pour un type particulier ou les types de notification sur une entrée de carnet d’adresses. Les types de notification sont indiqués par le masque d’événement passé avec le paramètre _ulEventMask_ . 
  
MAPI transfère cet appel **Advise** pour le fournisseur de carnet d’adresses qui est responsable de l’entrée telle qu’indiquée par l’identificateur d’entrée dans le paramètre _lpEntryID_ . Le fournisseur de carnet d’adresses gère l’inscription proprement dite ou appelle la méthode de prise en charge, [IMAPISupport::Subscribe](imapisupport-subscribe.md), pour demander MAPI pour inscrire l’appelant. Un numéro de connexion différente de zéro est renvoyé pour représenter l’inscription réussie.
  
Chaque fois qu’une modification est apportée à l’entrée du type indiqué par l’inscription de notification, le fournisseur de carnet d’adresses appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise spécifié dans le paramètre _lpAdviseSink_ . La méthode **OnNotify** inclut une structure [NOTIFICATION](notification.md) comme paramètre d’entrée qui contient des données pour l’événement. 
  
Selon le fournisseur de carnet d’adresses, l’appel de **OnNotify** peut se produire immédiatement après la modification de l’objet inscrit ou à une date ultérieure. Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut se produire sur n’importe quel thread. Les clients peuvent demander que ces notifications se produisent sur un thread particulier en appelant la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer l’objet récepteur advise qui est transmis à **Advise**. 
  
Car un fournisseur de carnet d’adresses peut libérer l’objet de récepteur advise passé par les clients à tout moment après l’exécution réussie de **notification** d’appel et avant une [IAddrBook::Unadvise](iaddrbook-unadvise.md) pour annuler la notification d’appel, les clients doivent version leurs objets récepteur advise **Advise** retourne. 
  
Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

