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
ms.openlocfilehash: ba93cd0343121751ab12514fe3f09e5a480d5b23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582272"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit un objet état qui a été affecté par une modification. 
  
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
  
> Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** . 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée de l’objet état modifié.
    
 **cValues**
  
> Nombre de structures [SPropValue](spropvalue.md) dans le tableau indiqué par le membre **lpPropVals** . 
    
 **lpPropVals**
  
> Pointeur vers un tableau de structures **SPropValue** qui décrivent les propriétés de l’objet état modifié. 
    
## <a name="remarks"></a>Remarques

La structure **STATUS_OBJECT_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) . La structure **STATUS_OBJECT_NOTIFICATION** est incluse dans une notification d’objet état pour un événement de type _fnevStatusObjectModified_. Notification d’état d’objet est une notification MAPI interne ; clients et fournisseurs de services ne peut pas inscrire pour qu’il et il ne peut pas générer des fournisseurs de services.
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événements](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

