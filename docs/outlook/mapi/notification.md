---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280098"
---
# <a name="notification"></a>NOTIFICATION
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un événement qui s'est produit et sur les données qui ont été affectées par l'événement.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a>Members

**ulEventType**
  
> Type d'événement de notification qui s'est produit. La valeur du membre **ulEventType** correspond à la structure incluse dans l'Union d' **informations** . Le membre **ulEventType** peut prendre la valeur de l'une des valeurs suivantes: 
    
 _fnevCriticalError_
  
> Une erreur globale s'est produite, telle qu'une session a été arrêtée en cours. Le membre **info** contient une structure [ERROR_NOTIFICATION](error_notification.md) . 
    
 _fnevExtended_
  
> Un événement interne défini par un fournisseur de services particulier s'est produit. Le membre **info** contient une structure [EXTENDED_NOTIFICATION](extended_notification.md) . 
    
 _fnevNewMail_
  
> Un message a été remis dans le dossier de réception approprié pour la classe de message et est en attente de traitement. Le membre **info** contient une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) . 
    
 _fnevObjectCopied_
  
> Un objet MAPI a été copié. Le membre **info** contient une structure [OBJECT_NOTIFICATION](object_notification.md) . 
    
 _fnevObjectCreated_
  
> Un objet MAPI a été créé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevObjectDeleted_
  
> Un objet MAPI a été supprimé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevObjectModified_
  
> Un objet MAPI a été modifié. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevObjectMoved_
  
> Un objet de banque de messages ou de carnet d'adresses a été déplacé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevSearchComplete_
  
> Une opération de recherche est terminée et les résultats sont disponibles. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevTableModified_
  
> Les informations d'une table ont été modifiées. Le membre **info** contient une structure [TABLE_NOTIFICATION](table_notification.md) . 
    
**info**
  
> Union des structures de notification décrivant les données affectées pour un type d'événement particulier. La structure incluse dans le membre **info** dépend de la valeur du membre **ulEventType** . 
    
## <a name="remarks"></a>Remarques

Une ou plusieurs structures de notification sont transmises en tant que paramètres d'entrée avec chaque appel à la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de **notification** enregistré. Les structures de **notification** contiennent des informations sur les événements spécifiques qui se sont produits et décrivent les objets affectés. 
  
Avant que les clients ou fournisseurs de services recevant une notification puissent utiliser la structure pour traiter l'événement, ils doivent vérifier le type d'événement comme indiqué dans le membre **ulEventType** . Par exemple, l'exemple de code illustré ci-dessous vérifie l'arrivée d'un nouveau message et, lorsqu'il détecte un événement de ce type, imprime la classe de message du message. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d'événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d'ensemble générale des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Présentation de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Notification d'événement de prise en charge](supporting-event-notification.md) <br/> |Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Structures MAPI](mapi-structures.md)

