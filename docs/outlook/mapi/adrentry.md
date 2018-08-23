---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f3a62f6783e3b1a0a0423a08c7f5e866b42b81f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569175"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit les zéro ou plusieurs propriétés qui appartiennent à un destinataire.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Réservé ; doit être égal à zéro.
    
 **cValues**
  
> Nombre de propriétés dans le tableau de valeurs de propriété vers laquelle pointe le membre **rgPropVals** . Le membre **cValues** peut être égal à zéro. 
    
 **rgPropVals**
  
> Pointeur vers un tableau de valeurs de propriété décrivant les propriétés pour le destinataire. Le membre **rgPropVals** peut être NULL. 
    
## <a name="remarks"></a>Remarques

Une structure **ADRENTRY** décrit les propriétés qui appartiennent à un seul destinataire. Les propriétés qui sont généralement utilisées pour décrire un destinataire sont les suivantes : 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Lorsqu’un identificateur d’entrée ou de la propriété **PR_ENTRYID** apparaît dans le tableau [SPropValue](spropvalue.md) pour un destinataire, cela indique que le destinataire a été résolu. Les clients appeler la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour vous assurer que tous les destinataires dans la liste des destinataires d’un message sortant ont été résolus. Seuls les destinataires résolus peuvent être envoyés avec des messages. 
  
 Structures **ADRENTRY** sont généralement combinées pour former un tableau pour le membre **aEntries** d’une structure [ADRLIST](adrlist.md) . 
  
 Structures de **ADRENTRY** et [SRow](srow.md) sont identiques, car ils permettent tous deux contient un membre réservé, un tableau de valeurs de propriété et un nombre de valeurs dans le tableau. Tandis que les structures **ADRENTRY** sont combinés pour former le membre **aEntries** d’une structure **ADRLIST** , structures **SRow** sont combinés pour former le membre **: UGAL** d’une structure [SRowSet](srowset.md) . Les deux types de structures de suivent les mêmes règles d’affectation, ce qui implique qu’une structure **SRowSet** qui est récupérée à partir de la table des matières d’un conteneur de carnet d’adresses peut être castée en une structure **ADRLIST** et utilisée comme est. 
  
Une structure **ADRENTRY** peut être vide. Par exemple, une structure **ADRENTRY** qui se trouve dans la structure **ADRLIST** désignée par le paramètre _lppAdrList_ dans un appel à **IAddrBook::Address** peut être vide lorsqu’un destinataire est supprimé. 
  
Pour plus d’informations sur la façon d’allouer de la mémoire pour les structures **ADRENTRY** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Structures MAPI](mapi-structures.md)

