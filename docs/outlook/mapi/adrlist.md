---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2fdcc3d343eaabf0b34ae9e82099f9c467772868
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572122"
---
# <a name="adrlist"></a>ADRLIST

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit zéro ou plusieurs propriétés appartenant à un ou plusieurs destinataires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Nombre d’entrées dans le tableau spécifié par **le membre aEntries.** 
    
**aEntries**
  
> Tableau de structures [ADRENTRY,](adrentry.md) une structure pour chaque destinataire. 
    
## <a name="remarks"></a>Remarques

Une structure **ADRLIST** contient une ou plusieurs structures **ADRENTRY** décrivant chacune les propriétés d’un destinataire. Un destinataire peut être non résolu. Cela signifie qu’il n’existe pas d’identificateur d’entrée dans son tableau de valeurs de propriétés. Un destinataire résolu signifie que la propriété **\_ PR ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse. En règle générale, les destinataires résolus ont également une adresse de messagerie PR_EMAIL_ADDRESS **(** [PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) propriété. Toutefois, l’adresse de messagerie n’est pas obligatoire. Les structures **ADRLIST** sont utilisées, par exemple, pour décrire la liste des destinataires d’un message sortant et par MAPI pour afficher les entrées dans le carnet d’adresses. 
  
Les structures **ADRLIST** ressemblent à des structures [SRowSet](srowset.md) utilisées pour représenter des lignes dans les tableaux. En fait, ces deux structures sont conçues pour pouvoir être utilisées indifféremment. Les deux contiennent un tableau de structures décrivant un groupe de propriétés et un décompte des valeurs dans le tableau. Alors que dans la structure **ADRLIST,** le tableau contient des structures [ADRENTRY,](adrentry.md) dans la structure **SRowSet,** le tableau contient des structures [SRow.](srow.md) Les structures **ADRENTRY** et **SRow** sont identiques dans la disposition. Étant donné que les structures **ADRLIST** et **SRowSet** suivent les mêmes règles d’allocation, une structure **SRowSet** récupérée à partir de la table des matières d’un conteneur de carnet d’adresses peut être castée vers une structure **ADRLIST** et utilisée telle qu’elle est. 
  
L’illustration suivante montre la disposition d’une structure **ADRLIST.** 
  
**Composants ADRLIST**
  
![Composants ADRLIST](media/amapi_18.gif "Composants ADRLIST")
  
Les **parties ADRENTRY** et [SPropValue](spropvalue.md) d’une structure **ADRLIST** doivent être allouées et libérées indépendamment des autres parties. Autrement dit, chaque structure **SPropValue** doit être allouée individuellement une fois que la mémoire de la structure **ADRENTRY a** été allouée et libérée avant la libération de la structure **ADRENTRY.** Cette indépendance dans la gestion de la mémoire permet aux destinataires et aux propriétés des destinataires individuels d’être librement ajoutés ou supprimés de la liste d’adresses. 
  
Les [fonctions MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) doivent être utilisées pour allouer et libérer la structure **ADRLIST** et tous ses composants. 
  
Si une liste de destinataires est trop grande pour tenir dans la mémoire, les clients peuvent appeler la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) pour travailler avec un sous-ensemble de la liste. Dans ce cas, les clients ne doivent pas utiliser les boîtes de dialogue communes du carnet d’adresses. 
  
Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRENTRY,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Voir aussi

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Structures MAPI](mapi-structures.md)

