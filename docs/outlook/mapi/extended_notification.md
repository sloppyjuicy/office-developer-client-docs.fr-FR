---
title: EXTENDED_NOTIFICATION
description: EXTENDED_NOTIFICATION décrit les informations relatives à un événement spécifique au fournisseur de services.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
ms.openlocfilehash: 80d0f0d63956f3b8fc67f9a05280e0ce52015b13
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817941"
---
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations relatives à un événement spécifique au fournisseur de services. 
  
|Propriété |Valeur |
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
  
> Pointeur vers des paramètres spécifiques à un événement. Le type de paramètres utilisés dépend de la valeur du membre **ulEvent** ; ces paramètres sont documentés par le fournisseur qui a émis l’événement. 
    
## <a name="remarks"></a>Remarques

La **structure EXTENDED_NOTIFICATION** est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION](notification.md) . Lorsque le membre **d’informations** d’une structure **NOTIFICATION** contient une structure **EXTENDED_NOTIFICATION** , le membre **ulEventType** de la structure **NOTIFICATION** est défini sur  _fnevExtended_.
  
L’événement étendu est défini par un fournisseur de services pour représenter un type de modification qui ne peut être couvert par aucun des autres événements prédéfinis. Seuls les clients qui savent avant d’inscrire qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire à cet événement. Il n’est pas possible pour les clients de déterminer sans connaissance avancée si un fournisseur de services prend en charge un événement étendu. Si un fournisseur de services prend en charge un événement étendu, il montre comment gérer un tel événement lorsqu’il est reçu.
  
Une notification étendue est envoyée par la session lorsqu’un client se déconnecte. Inscrivez-vous à cette notification en appelant [IMAPISession::Advise](imapisession-advise.md) avec le paramètre  _lpEntryID_ défini sur NULL et le paramètre  _cbEntryID_ défini sur zéro. 
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble générale des événements de notification et de notification. |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications. |
|[Prise en charge de la notification d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport](imapisupportiunknown.md) pour générer des notifications. |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

