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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430167"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un objet qui a subi une modification, comme une opération de copie ou de modification.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l'identificateur d'entrée de l'objet affecté.
    
 **ulObjType**
  
> Type d'objet affecté. Les types possibles sont les suivants:
    
MAPI_STORE 
  
> Banque de messages. 
    
MAPI_ADDRBOOK 
  
> Carnet d'adresses. 
    
MAPI_FOLDER 
  
> Sous.
    
MAPI_ABCONT 
  
> Conteneur de carnet d'adresses.
    
MAPI_MESSAGE 
  
> Message.
    
MAPI_MAILUSER 
  
> Utilisateur de messagerie.
    
MAPI_ATTACH 
  
> Connexion.
    
MAPI_DISTLIST 
  
> Liste de distribution.
    
MAPI_PROFSECT 
  
> Section profil.
    
MAPI_STATUS 
  
> Objet Status.
    
MAPI_SESSION 
  
> Objet session.
    
 **cbParentID**
  
> Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpParentID** . 
    
 **lpParentID**
  
> Pointeur vers l'identificateur d'entrée du parent de l'objet affecté.
    
 **cbOldID**
  
> Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpOldID** . 
    
 **lpOldID**
  
> Pointeur vers l'identificateur d'entrée de l'objet d'origine. Ce pointeur peut être NULL si l'événement ne requiert pas d'objet d'origine.
    
 **cbOldParentID**
  
> Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpOldParentID** . 
    
 **lpOldParentID**
  
> Pointeur vers l'identificateur d'entrée du parent de l'objet d'origine. Ce pointeur peut être NULL si l'événement ne requiert pas d'objet d'origine.
    
 **lpPropTagArray**
  
> Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient les balises de propriété qui identifient les propriétés affectées par l'événement. 
    
## <a name="remarks"></a>Remarques

La structure **OBJECT_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) . Lorsque le membre **info** d'une structure de **notification** contient une structure **OBJECT_NOTIFICATION** , le membre **ulEventType** de la structure de **notification** est défini sur l'un des types d'événements suivants: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
L'événement de recherche terminée, représenté par le type d'événement fnevSearchComplete, indique que la recherche initiale du domaine pour un dossier de recherche est terminée.
  
Les membres suivants qui contiennent des informations sur l'objet d'origine sont utilisés uniquement dans les événements de déplacement et de copie. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Ces membres ne s'appliquent pas aux autres types d'événements.
  
Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d'événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d'ensemble générale des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Présentation de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Notification d'événement de prise en charge](supporting-event-notification.md) <br/> |Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Structures MAPI](mapi-structures.md)

