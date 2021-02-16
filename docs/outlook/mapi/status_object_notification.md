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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426267"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un objet d’état qui a été affecté par une modification. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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
  
> Nombre d’octets dans l’identificateur d’entrée pointé par le membre **lpEntryID.** 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée de l’objet d’état modifié.
    
 **cValues**
  
> Nombre de structures [SPropValue](spropvalue.md) dans le tableau pointées par le membre **lpPropVals.** 
    
 **lpPropVals**
  
> Pointeur vers un tableau de structures **SPropValue** qui décrivent les propriétés de l’objet d’état modifié. 
    
## <a name="remarks"></a>Remarques

La **STATUS_OBJECT_NOTIFICATION** structure est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION.](notification.md) La **STATUS_OBJECT_NOTIFICATION** structure est incluse avec une notification d’objet d’état pour un événement de type  _fnevStatusObjectModified_. La notification d’objet d’état est une notification MAPI interne ; les clients et les fournisseurs de services ne peuvent pas s’y inscrire et les fournisseurs de services ne peuvent pas le générer.
  
Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

