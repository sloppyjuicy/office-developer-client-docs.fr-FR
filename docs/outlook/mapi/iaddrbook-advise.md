---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6c2cd84df8f45bd69f4fd78f492afcde1fcdd7c6
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463656"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre un client ou un fournisseur de services pour recevoir des notifications concernant les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses, de l’utilisateur de messagerie ou de la liste de distribution qui génère une notification lorsqu’une modification se produit du ou des types décrits dans le paramètre _ulEventMask_ . 
    
 _ulEventMask_
  
> [in] Un ou plusieurs événements de notification que l’appelant inscrit pour recevoir. Chaque événement est associé à une structure de notification particulière qui contient des informations sur la modification qui s’est produite. Le tableau suivant répertorie les valeurs valides  _pour ulEventMask_ et leurs structures correspondantes. 
    
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
  
> [in] Pointeur vers l’objet de réception de notification à appeler lorsque l’événement pour lequel une notification a été demandée se produit.
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro de connexion autre que zéro qui représente l’inscription de la notification.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> Le fournisseur de carnet d’adresses responsable de l’identificateur d’entrée transmis  _dans lpEntryID_ n’a pas pu enregistrer de notification pour l’entrée correspondante. 
    
MAPI_E_NO_SUPPORT 
  
> La notification n’est pas prise en charge par le fournisseur de carnet d’adresses responsable de l’objet identifié par l’identificateur d’entrée transmis dans _le paramètre lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée transmis  _dans lpEntryID_ ne peut être géré par aucun des fournisseurs de carnet d’adresses dans le profil. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la **méthode Advise** pour s’inscrire à un type particulier ou à des types de notifications sur une entrée de carnet d’adresses. Les types de notification sont indiqués par le masque d’événement transmis avec le  _paramètre ulEventMask_ . 
  
MAPI a transmis cet appel **Advise** au fournisseur de carnet d’adresses responsable de l’entrée, comme indiqué par l’identificateur d’entrée dans le paramètre _lpEntryID_ . Le fournisseur de carnet d’adresses gère l’inscription proprement dite ou appelle la méthode de support, [IMAPISupport::Subscribe](imapisupport-subscribe.md), pour demander à MAPI d’inscrire l’appelant. Un numéro de connexion autre que zéro est renvoyé pour représenter l’inscription réussie.
  
Chaque fois qu’une modification a lieu sur l’entrée du type indiqué par l’inscription de notification, le fournisseur de carnet d’adresses appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de réception de notification spécifié dans le paramètre _lpAdviseSink_ . La **méthode OnNotify inclut** une structure [NOTIFICATION](notification.md) en tant que paramètre d’entrée qui contient des données pour décrire l’événement. 
  
Selon le fournisseur de carnet d’adresses, l’appel à **OnNotify** peut se produire immédiatement après la modification de l’objet inscrit ou ultérieurement. Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut se produire sur n’importe quel thread. Les clients peuvent demander que ces notifications se produisent sur un thread particulier en appelant la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer l’objet de réception de notification qui est transmis à **Advise**. 
  
Étant donné qu’un fournisseur de carnet d’adresses peut libérer l’objet de réception de notification transmis par les  clients à tout moment après l’exécution de l’appel Advise et avant un appel [IAddrBook::Unadvise](iaddrbook-unadvise.md) pour annuler la notification, les clients doivent libérer leurs objets de réception de notification lors du retour de **Advise**. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notification](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

