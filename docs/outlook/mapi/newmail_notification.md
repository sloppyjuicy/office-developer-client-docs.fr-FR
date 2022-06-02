---
title: NEWMAIL_NOTIFICATION
description: Fournit les informations de propriété, les membres et les remarques pour NEWMAIL_NOTIFICATION, qui décrit les informations relatives à l’arrivée d’un nouveau message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
ms.openlocfilehash: 18dc74dd2fbcdea10cb820b075e2ac6fd184bc1e
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852508"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations relatives à l’arrivée d’un nouveau message. 
  
|Propriété |Valeur |
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
  
> Nombre d’octets dans l’identificateur d’entrée pointé par le membre **lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée du message nouvellement arrivé.
    
 **cbParentID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par le membre **lpParentID** . 
    
 **lpParentID**
  
> Pointeur vers l’identificateur d’entrée du dossier de réception pour le message nouvellement arrivé.
    
 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour décrire le format des propriétés de chaîne incluses dans le message. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
 **lpszMessageClass**
  
> Pointeur vers la classe de message du message nouvellement arrivé. 
    
 **ulMessageFlags**
  
> Masque de bits des indicateurs qui décrit l’état actuel du message nouvellement arrivé. Le membre **ulMessageFlags** est une copie de la propriété **PR_MESSAGE_FLAGS** du message ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
## <a name="remarks"></a>Remarques

La **structure NEWMAIL_NOTIFICATION** est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION](notification.md) . Lorsque le membre **d’informations** d’une structure **NOTIFICATION** contient une structure **NEWMAIL_NOTIFICATION** , le membre **ulEventType** de la structure **NOTIFICATION** est défini sur  _fnevNewMail._
  
MAPI utilise la structure **NEWMAIL_NOTIFICATION** uniquement en tant que membre de la structure **NOTIFICATION** , qui contient des informations sur un événement de notification pour le récepteur de conseils. 
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble générale des événements de notification et de notification. |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications. |
|[Prise en charge de la notification d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications. |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Structures MAPI](mapi-structures.md)

