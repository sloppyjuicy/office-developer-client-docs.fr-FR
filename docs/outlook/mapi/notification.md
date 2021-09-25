---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eff140179865d662545d0e21ca3789a6e8c2643b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583974"
---
# <a name="notification"></a>NOTIFICATION
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un événement qui s’est produit et les données qui ont été affectées par l’événement.
  
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

## <a name="members"></a>Members

**ulEventType**
  
> Type d’événement de notification qui s’est produit. La valeur du membre **ulEventType** correspond à la structure incluse dans l’union **d’informations.** Le **membre ulEventType** peut être définie sur l’une des valeurs suivantes : 
    
 _fnevCriticalError_
  
> Une erreur globale s’est produite, telle qu’une session en cours d’arrêt. Le **membre d’informations** contient [ERROR_NOTIFICATION](error_notification.md) structure. 
    
 _fnevExtended_
  
> Un événement interne défini par un fournisseur de services particulier s’est produit. Le **membre d’informations** contient une structure [EXTENDED_NOTIFICATION](extended_notification.md) de données. 
    
 _fnevNewMail_
  
> Un message a été remis au dossier de réception approprié pour la classe de message et attend d’être traitée. Le **membre d’informations** contient [une structure NEWMAIL_NOTIFICATION](newmail_notification.md) de données. 
    
 _fnevObjectCopied_
  
> Un objet MAPI a été copié. Le **membre d’informations** contient une structure [OBJECT_NOTIFICATION](object_notification.md) de données. 
    
 _fnevObjectCreated_
  
> Un objet MAPI a été créé. Le **membre d’informations** contient une structure **OBJECT_NOTIFICATION** de données. 
    
 _fnevObjectDeleted_
  
> Un objet MAPI a été supprimé. Le **membre d’informations** contient une structure **OBJECT_NOTIFICATION** de données. 
    
 _fnevObjectModified_
  
> Un objet MAPI a changé. Le **membre d’informations** contient une structure **OBJECT_NOTIFICATION** de données. 
    
 _fnevObjectMoved_
  
> Un objet de magasin de messages ou de carnet d’adresses a été déplacé. Le **membre d’informations** contient une structure **OBJECT_NOTIFICATION** de données. 
    
 _fnevSearchComplete_
  
> Une opération de recherche est terminée et les résultats sont disponibles. Le **membre d’informations** contient une structure **OBJECT_NOTIFICATION** de données. 
    
 _fnevTableModified_
  
> Les informations d’un tableau ont changé. Le **membre d’informations** contient une structure [TABLE_NOTIFICATION](table_notification.md) de données. 
    
**info**
  
> Union de structures de notification décrivant les données affectées pour un type particulier d’événement. La structure incluse dans le membre **d’informations** dépend de la valeur du **membre ulEventType.** 
    
## <a name="remarks"></a>Remarques

Une ou plusieurs structures **de NOTIFICATION** sont transmises en tant que paramètres d’entrée à chaque appel à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) d’un sink de notification inscrit. Les **structures NOTIFICATION** contiennent des informations sur les événements particuliers qui se sont produits et décrivent les objets affectés. 
  
Avant que les clients ou fournisseurs de services recevant une notification ne peuvent utiliser la structure pour traiter l’événement, ils doivent vérifier le type d’événement comme indiqué dans le membre **ulEventType.** Par exemple, l’exemple de code présenté ici vérifie l’arrivée d’un nouveau message et, lorsqu’il détecte un événement de ce type, imprime la classe de message du message. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Structures MAPI](mapi-structures.md)

