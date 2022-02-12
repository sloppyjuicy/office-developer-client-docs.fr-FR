---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b89beabba6b6308a78953e5be0e6879fb66683ec
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776220"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un objet qui a subi une modification, par exemple en cours de copie ou de modification.
  
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
  
> Nombre d’octets dans l’identificateur d’entrée pointé par **le membre lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée de l’objet affecté.
    
 **ulObjType**
  
> Type d’objet affecté. Les types possibles sont les suivants :
    
MAPI_STORE 
  
> Magasin de messages. 
    
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
  
> Pièce jointe.
    
MAPI_DISTLIST 
  
> Liste de distribution.
    
MAPI_PROFSECT 
  
> Section Profil.
    
MAPI_STATUS 
  
> Objet Status.
    
MAPI_SESSION 
  
> Objet Session.
    
 **cbParentID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par **le membre lpParentID** . 
    
 **lpParentID**
  
> Pointeur vers l’identificateur d’entrée du parent de l’objet affecté.
    
 **cbOldID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par **le membre lpOldID** . 
    
 **lpOldID**
  
> Pointeur vers l’identificateur d’entrée de l’objet d’origine. Ce pointeur peut avoir la valeur NULL si l’événement ne nécessite pas d’objet d’origine.
    
 **cbOldParentID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par **le membre lpOldParentID** . 
    
 **lpOldParentID**
  
> Pointeur vers l’identificateur d’entrée du parent de l’objet d’origine. Ce pointeur peut avoir la valeur NULL si l’événement ne nécessite pas d’objet d’origine.
    
 **lpPropTagArray**
  
> Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient les balises de propriété identifiant les propriétés affectées par l’événement. 
    
## <a name="remarks"></a>Remarques

La **OBJECT_NOTIFICATION** structure est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION](notification.md) . Lorsque le membre **d’informations** d’une structure **NOTIFICATION** contient une structure **OBJECT_NOTIFICATION** , le membre **ulEventType** de la structure **NOTIFICATION** est définie sur l’un des types d’événements suivants : 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
L’événement de recherche complet, représenté par le type d’événement fnevSearchComplete, indique que la recherche initiale du domaine pour un dossier de recherche est terminée.
  
Les membres suivants qui contiennent des informations sur l’objet d’origine sont utilisés uniquement dans les événements de déplacement et de copie. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Ces membres ne s’appliquent pas aux autres types d’événements.
  
Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification. |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications. |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications. |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Structures MAPI](mapi-structures.md)

