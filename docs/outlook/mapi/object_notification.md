---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 876c8fc3667929e3c2e7403e71e6d392981d34f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573354"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient des informations sur un objet qui a subi une modification, tel qu’en cours copié ou modifié.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée de l’objet concerné.
    
 **ulObjType**
  
> Type d’objet affecté. Les types possibles sont les suivantes :
    
MAPI_STORE 
  
> Banque de messages. 
    
MAPI_ADDRBOOK 
  
> Carnet d’adresses. 
    
MAPI_FOLDER 
  
> Dossier.
    
MAPI_ABCONT 
  
> Conteneur de carnet d’adresses.
    
MAPI_MESSAGE 
  
> Message.
    
MAPI_MAILUSER 
  
> Utilisateur de messagerie.
    
MAPI_ATTACH 
  
> Objet Attachment.
    
MAPI_DISTLIST 
  
> Liste de distribution.
    
MAPI_PROFSECT 
  
> Section de profil.
    
MAPI_STATUS 
  
> Objet d’état.
    
MAPI_SESSION 
  
> Objet de la session.
    
 **cbParentID**
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpParentID** . 
    
 **lpParentID**
  
> Pointeur vers l’identificateur d’entrée du parent de l’objet concerné.
    
 **cbOldID**
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpOldID** . 
    
 **lpOldID**
  
> Pointeur vers l’identificateur d’entrée de l’objet d’origine. Ce pointeur peut être NULL si l’événement ne nécessite pas d’un objet d’origine.
    
 **cbOldParentID**
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpOldParentID** . 
    
 **lpOldParentID**
  
> Pointeur vers l’identificateur d’entrée du parent de l’objet d’origine. Ce pointeur peut être NULL si l’événement ne nécessite pas d’un objet d’origine.
    
 **lpPropTagArray**
  
> Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient les étiquettes de propriété identifiant les propriétés affectées par l’événement. 
    
## <a name="remarks"></a>Remarques

La structure **OBJECT_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) . Lorsque le membre **d’informations** d’une structure **NOTIFICATION** contient une structure **OBJECT_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur un des types suivants d’événements : 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
L’événement complete de recherche, représenté par le type d’événement fnevSearchComplete, indique que la recherche initiale du domaine pour un dossier de recherche est terminée.
  
Les membres suivants qui contiennent des informations sur l’objet d’origine sont utilisés uniquement dans les événements de déplacement et de copie. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Ces membres ne s’appliquent pas aux autres types d’événements.
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événements](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Structures MAPI](mapi-structures.md)

