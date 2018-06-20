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
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784929"
---
# <a name="notification"></a>NOTIFICATION
 
**S’applique à**: Outlook 
  
Contient des informations sur un événement qui s’est produite et les données qui a été affectées par l’événement.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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

## <a name="members"></a>Membres

**ulEventType**
  
> Type d’événement de notification qui s’est produite. La valeur du membre **ulEventType** correspond à la structure qui est incluse dans l’union **info** . Le membre **ulEventType** peut être défini sur une des valeurs suivantes : 
    
 _fnevCriticalError_
  
> Une erreur globale s’est produite, par exemple une session d’arrêt en cours. Le membre **info** contient une structure [ERROR_NOTIFICATION](error_notification.md) . 
    
 _fnevExtended_
  
> Un événement interne définie par un fournisseur de services particulier s’est produite. Le membre **info** contient une structure [EXTENDED_NOTIFICATION](extended_notification.md) . 
    
 _fnevNewMail_
  
> Un message a été remis vers le dossier pour la classe de message de réception et est en attente de traitement. Le membre **info** contient une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) . 
    
 _fnevObjectCopied_
  
> Un objet MAPI a été copié. Le membre **info** contient une structure [OBJECT_NOTIFICATION](object_notification.md) . 
    
 _fnevObjectCreated_
  
> Un objet MAPI a été créé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevObjectDeleted_
  
> Un objet MAPI a été supprimé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevObjectModified_
  
> Un objet MAPI a changé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevObjectMoved_
  
> Une banque de messages ou l’adresse livre objet a été déplacé. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevSearchComplete_
  
> Une opération de recherche est terminée et les résultats sont disponibles. Le membre **info** contient une structure **OBJECT_NOTIFICATION** . 
    
 _fnevTableModified_
  
> Informations contenues dans un tableau a été modifiée. Le membre **info** contient une structure [TABLE_NOTIFICATION](table_notification.md) . 
    
**Info**
  
> Union de structures de notification décrivant les données d’un type particulier d’événement affectées. La structure incluse dans le membre **info** dépend de la valeur du membre **ulEventType** . 
    
## <a name="remarks"></a>Remarques

Une ou plusieurs des structures **NOTIFICATION** sont passés comme paramètres d’entrée à chaque appel de méthode [d’IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) d’un récepteur de notifications enregistrés. Les structures **NOTIFICATION** contiennent des informations sur les événements qui se sont produites et décrivent les objets affectés. 
  
Avant que les clients ou fournisseurs de services de recevoir une notification puissent utiliser la structure à traiter l’événement, ils doivent vérifier le type d’événement comme indiqué dans le membre **ulEventType** . L’exemple de code qui est présenté ici vérifie l’arrivée d’un nouveau message et lors de la détection d’un événement de ce type, par exemple, imprime la classe de message du message. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gérer les Notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge de la Notification d’événement](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Structures MAPI](mapi-structures.md)

