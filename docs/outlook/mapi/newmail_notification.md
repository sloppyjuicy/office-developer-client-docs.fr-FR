---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784902"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**S’applique à**: Outlook 
  
Décrit les informations qui sont associées à l’arrivée d’un nouveau message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a>Membres

 **cbEntryID**
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée du message qui vient d’arriver.
    
 **cbParentID**
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpParentID** . 
    
 **lpParentID**
  
> Pointeur vers l’identificateur d’entrée du dossier de réception pour le message qui vient d’arriver.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour décrire le format des propriétés de chaîne inclus dans le message. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **lpszMessageClass**
  
> Pointeur vers la classe de message du message qui vient d’arriver. 
    
 **ulMessageFlags**
  
> Masque de bits d’indicateurs qui décrit l’état actuel du message qui vient d’arriver. Le membre **ulMessageFlags** est une copie de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.
    
## <a name="remarks"></a>Remarques

La structure **NEWMAIL_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) . Lorsque le membre **info** d’une structure **NOTIFICATION** contient une structure **NEWMAIL_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur _fnevNewMail._
  
MAPI utilise la structure **NEWMAIL_NOTIFICATION** uniquement en tant que membre de la structure **NOTIFICATION** , qui conserve des informations sur un événement de notification pour le récepteur de notifications. 
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gérer les Notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge de la Notification d’événement](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Structures MAPI](mapi-structures.md)

