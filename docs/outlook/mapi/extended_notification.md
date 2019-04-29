---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415718"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations relatives à un événement qui est spécifique au fournisseur de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>Members

 **ulEvent**
  
> Code d'événement étendu défini par le fournisseur.
    
 **cb**
  
> Nombre d'octets dans les paramètres spécifiques de l'événement pointés par **pbEventParameters**. 
    
 **pbEventParameters**
  
> Pointeur vers des paramètres spécifiques à l'événement. Le type de paramètres utilisés dépend de la valeur du membre **ulEvent** ; ces paramètres sont documentés par le fournisseur qui a émis l'événement. 
    
## <a name="remarks"></a>Remarques

La structure **EXTENDED_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) . Lorsque le membre **info** d'une structure de **notification** contient une structure **EXTENDED_NOTIFICATION** , le membre **ulEventType** de la structure de **notification** est défini sur _fnevExtended_.
  
L'événement étendu est défini par un fournisseur de services pour représenter un type de modification qui ne peut pas être couvert par les autres événements prédéfinis. Seuls les clients qui connaissent qu'un fournisseur de services prend en charge un événement étendu peuvent s'inscrire à cet événement. Il n'est pas possible pour les clients de déterminer sans connaissances avancées si un fournisseur de services prend en charge un événement étendu. Si un fournisseur de services prend en charge un événement étendu, il montre comment gérer ce type d'événement lors de sa réception.
  
Une notification étendue est envoyée par la session lorsqu'un client se déconnecte. Inscrivez-vous à cette notification en appelant [IMAPISession:: Advise](imapisession-advise.md) avec le paramètre _LPENTRYID_ défini sur null et le paramètre _cbEntryID_ défini sur zéro. 
  
Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d'événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d'ensemble générale des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Présentation de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Notification d'événement de prise en charge](supporting-event-notification.md) <br/> |Présentation de la façon dont les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

