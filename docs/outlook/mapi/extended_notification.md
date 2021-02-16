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
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations liées à un événement spécifique au fournisseur de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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
  
> Code d’événement étendu défini par le fournisseur.
    
 **cb**
  
> Nombre d’octets dans les paramètres spécifiques à l’événement pointés par **pbEventParameters**. 
    
 **pbEventParameters**
  
> Pointeur vers des paramètres spécifiques à l’événement. Le type de paramètres utilisés dépend de la valeur du **membre ulEvent** ; ces paramètres sont documentés par le fournisseur qui a émis l’événement. 
    
## <a name="remarks"></a>Remarques

La **EXTENDED_NOTIFICATION** structure est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION.](notification.md) Lorsque le **membre d’informations** d’une structure **notification** contient une structure **EXTENDED_NOTIFICATION,** le membre **ulEventType** de la structure **NOTIFICATION** est définie sur  _fnevExtended_.
  
L’événement étendu est défini par un fournisseur de services pour représenter un type de modification qui ne peut être couvert par aucun autre événement prédéféré. Seuls les clients qui savent avant qu’ils s’inscrivent qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire à cet événement. Il n’est pas possible pour les clients de déterminer sans connaissances avancées si un fournisseur de services prend en charge un événement étendu. Si un fournisseur de services prend en charge un événement étendu, il indique comment gérer un tel événement lorsqu’il est reçu.
  
Une notification étendue est envoyée par la session lorsqu’un client se déconnecte. Inscrivez-vous à cette notification en appelant [IMAPISession::Advise](imapisession-advise.md) avec le paramètre  _lpEntryID_ sur NULL et le paramètre  _cbEntryID_ sur zéro. 
  
Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

