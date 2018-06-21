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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19783281"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**S’applique à**: Outlook 
  
Décrit les informations relatives à un événement qui est spécifique au fournisseur de service. 
  
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

## <a name="members"></a>Membres

 **ulEvent**
  
> Code d’événement étendue définie par le fournisseur.
    
 **cb**
  
> Nombre d’octets dans les paramètres spécifiques à l’événement indiqué par **pbEventParameters**. 
    
 **pbEventParameters**
  
> Pointeur vers les paramètres spécifiques à l’événement. Le type de paramètres qui sont utilisés dépend de la valeur du membre **ulEvent** ; Ces paramètres sont décrits par le fournisseur qui a émis l’événement. 
    
## <a name="remarks"></a>Remarques

La structure **EXTENDED_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) . Lorsque le membre **info** d’une structure **NOTIFICATION** contient une structure **EXTENDED_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur _fnevExtended_.
  
L’événement étendue est définie par un fournisseur de services pour représenter un type de modification qui ne peuvent pas être couvertes par les autres événements prédéfinis. Seuls les clients qui savoir avant qu’ils inscrivent qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire pour cet événement. Il n’est pas possible pour les clients déterminer sans connaissances avancées si un fournisseur de services prend en charge un événement étendu. Si un fournisseur de services prend en charge un événement étendu, il montre comment gérer un événement lorsqu’il est reçu.
  
Une étendue est envoyé à la session quand un client se déconnecte. Enregistrer cette notification en appelant [IMAPISession::Advise](imapisession-advise.md) avec le paramètre _lpEntryID_ défini sur NULL et le paramètre _cbEntryID_ définir sur zéro. 
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gérer les Notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge de la Notification d’événement](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

