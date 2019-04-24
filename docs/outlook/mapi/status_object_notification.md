---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336441"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un objet Status qui a été affecté par une modification. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l'identificateur d'entrée de l'objet d'état modifié.
    
 **cValues**
  
> Nombre de structures [SPropValue](spropvalue.md) dans le tableau vers lequel pointe le membre **lpPropVals** . 
    
 **lpPropVals**
  
> Pointeur vers un tableau de structures **SPropValue** qui décrivent les propriétés de l'objet d'état modifié. 
    
## <a name="remarks"></a>Remarques

La structure **STATUS_OBJECT_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) . La structure **STATUS_OBJECT_NOTIFICATION** est incluse avec une notification d'objet d'État pour un événement de type _fnevStatusObjectModified_. La notification d'objet d'État est une notification MAPI interne; les clients et les fournisseurs de services ne peuvent pas s'inscrire à l'informatique et les fournisseurs de services ne peuvent pas le générer.
  
Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d'événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d'ensemble générale des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Présentation de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Notification d'événement de prise en charge](supporting-event-notification.md) <br/> |Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

