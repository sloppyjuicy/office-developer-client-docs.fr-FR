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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439855"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations liées à l’arrivée d’un nouveau message. 
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par le membre **lpEntryID.** 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée du message nouvellement arrivé.
    
 **cbParentID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par le membre **lpParentID.** 
    
 **lpParentID**
  
> Pointeur vers l’identificateur d’entrée du dossier de réception du message nouvellement arrivé.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour décrire le format des propriétés de chaîne incluses dans le message. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **lpszMessageClass**
  
> Pointeur vers la classe de message du message nouvellement arrivé. 
    
 **ulMessageFlags**
  
> Masque de bits d’indicateurs décrivent l’état actuel du message nouvellement arrivé. Le **membre ulMessageFlags est** une copie de la propriété PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). 
    
## <a name="remarks"></a>Remarques

La **NEWMAIL_NOTIFICATION** structure est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION.](notification.md) Lorsque le **membre d’informations** d’une structure **NOTIFICATION** contient une structure **NEWMAIL_NOTIFICATION,** le membre **ulEventType** de la structure **NOTIFICATION** est définie sur  _fnevNewMail._
  
MAPI utilise la structure **NEWMAIL_NOTIFICATION** uniquement en tant que membre de la structure **notification,** qui contient des informations sur un événement de notification pour le réception de notification. 
  
Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Structures MAPI](mapi-structures.md)

