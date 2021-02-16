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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421437"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit zéro ou plusieurs propriétés appartenant à un destinataire.
  
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
  
> Réservé ; doit être zéro.
    
 **cValues**
  
> Nombre de propriétés dans le tableau des valeurs de propriétés pointées par le **membre rgPropVals.** Le **membre cValues** peut être zéro. 
    
 **rgPropVals**
  
> Pointeur vers un tableau de valeurs de propriété décrivant les propriétés du destinataire. Le **membre rgPropVals peut** être NULL. 
    
## <a name="remarks"></a>Remarques

Une **structure ADRENTRY** décrit les propriétés qui appartiennent à un seul destinataire. Les propriétés généralement utilisées pour décrire un destinataire sont les suivantes : 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Lorsqu’un identificateur **d’entrée** ou PR_ENTRYID propriété s’affiche dans le tableau [SPropValue](spropvalue.md) d’un destinataire, cela indique que le destinataire a été résolu. Les clients appellent la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour s’assurer que tous les destinataires de la liste des destinataires d’un message sortant ont été résolus. Seuls les destinataires résolus peuvent être envoyés avec des messages. 
  
 Les structures **ADRENTRY** sont généralement combinées pour former un tableau pour le membre **aEntries** d’une structure [ADRLIST.](adrlist.md) 
  
 Les structures **ADRENTRY** et [SRow](srow.md) sont identiques, car elles contiennent toutes deux un membre réservé, un tableau de valeurs de propriétés et un nombre de valeurs dans le tableau. Tandis que les structures **ADRENTRY** sont combinées pour former le membre **aEntries** d’une structure **ADRLIST,** les structures **SRow** sont combinées pour former le membre **aRow** d’une structure [SRowSet.](srowset.md) Les deux types de structures suivent les mêmes règles d’allocation, ce qui signifie qu’une structure **SRowSet** récupérée à partir de la table des matières d’un conteneur de carnet d’adresses peut être castée vers une structure **ADRLIST** et utilisée telle qu’elle est. 
  
Une **structure ADRENTRY** peut être vide. Par exemple, une structure **ADRENTRY** contenue dans la structure **ADRLIST** pointée par le paramètre  _lppAdrList_ dans un appel à **IAddrBook::Address** peut être vide lorsqu’un destinataire est supprimé. 
  
Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRENTRY,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Structures MAPI](mapi-structures.md)

