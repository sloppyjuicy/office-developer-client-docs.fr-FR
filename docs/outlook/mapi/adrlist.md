---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 87b91b66807ce79533029a8d5b5c4956bc4d5ce9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565766"
---
# <a name="adrlist"></a>ADRLIST

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit les zéro ou plusieurs propriétés qui appartiennent à un ou plusieurs destinataires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Nombre d’entrées dans le tableau spécifié par le membre **aEntries** . 
    
**aEntries**
  
> Tableau de structures [ADRENTRY](adrentry.md) une structure pour chaque destinataire. 
    
## <a name="remarks"></a>Remarques

Une structure **ADRLIST** contient une ou plusieurs structures **ADRENTRY** , chacun décrivant les propriétés d’un destinataire. Un destinataire peut être résolu. Cela signifie qu’il manque un identificateur d’entrée dans le tableau des valeurs de propriété. Un destinataire résolu signifie que la **PR\_ENTRYID** propriété ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse. En règle générale, les destinataires résolus ont également un message électronique adresse de la propriété **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Toutefois, l’adresse de messagerie n’est pas requis. Par exemple, les structures **ADRLIST** sont utilisés pour décrire la liste de destinataires pour un message sortant et par MAPI pour afficher les entrées dans le carnet d’adresses. 
  
Structures **ADRLIST** ressembler à structures [SRowSet](srowset.md) les structures utilisées pour la représentation des lignes de tableaux. En fait, ces deux structures sont conçues pour être utilisées indifféremment. Les deux contient un tableau de structures décrivant un groupe de propriétés et un nombre de valeurs dans le tableau. Tandis que dans la structure **ADRLIST** , le tableau contient des structures [ADRENTRY](adrentry.md) , dans la structure **SRowSet** le tableau contient des structures de [SRow](srow.md) . Structures de **ADRENTRY** et **SRow** sont identiques dans la mise en page. Étant donné que les structures **ADRLIST** et **SRowSet** respectent les mêmes règles d’affectation, une structure **SRowSet** qui est récupérée à partir de la table des matières d’un conteneur de carnet d’adresses pouvant être castée en une structure **ADRLIST** et utilisée comme est. 
  
L’illustration suivante montre la disposition d’une structure **ADRLIST** . 
  
**Composants ADRLIST**
  
![Composants ADRLIST] (media/amapi_18.gif "Composants ADRLIST")
  
Les parties **ADRENTRY** et [SPropValue](spropvalue.md) dans une structure **ADRLIST** doivent être allouées et libérées indépendamment les autres composants. Autrement dit, chaque structure **SPropValue** doit être affecté individuellement une fois que la mémoire pour la structure **ADRENTRY** a été allouée et libérée avant la structure **ADRENTRY** est libérée. Cette indépendance dans la gestion de la mémoire permet de destinataires et les propriétés de destinataire individuelles pour être librement ajoutés ou supprimés de la liste d’adresses. 
  
Les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) doivent être utilisées pour allouer et libérer la structure **ADRLIST** et tous ses composants. 
  
Si une liste de destinataires est trop volumineux pour tenir dans la mémoire, les clients peuvent appeler la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) pour travailler avec un sous-ensemble de la liste. Les clients ne doivent pas utiliser l’adresse livre boîtes de dialogue courantes dans cette situation. 
  
Pour plus d’informations sur la façon d’allouer de la mémoire pour les structures **ADRENTRY** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Voir aussi

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Structures MAPI](mapi-structures.md)

