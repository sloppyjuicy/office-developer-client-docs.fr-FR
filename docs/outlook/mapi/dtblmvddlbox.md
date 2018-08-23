---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 910f779f3463ee5dccd052655a442ef24c2cce58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570680"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une liste déroulante qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Réservé ; doit être égal à zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING. Les différentes valeurs de cette propriété sont affichent comme des entrées distinctes dans la liste déroulante.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVDDLBOX** décrit une liste déroulante à valeurs multiples une liste en lecture seule d’éléments. En utilisant une liste déroulante à valeurs multiples, les valeurs sont affichées lorsqu’un utilisateur clique sur une barre de défilement. 
  
Les données qui sont affichées provient de la propriété identifiée dans le membre **ulMVPropTag** . Il n’existe aucune exigence pour lire à partir de l’interface de la propriété qui est associé à la table d’affichage. En outre, étant donné que les utilisateurs ne sont pas en mesure de réaliser des sélections à partir de ces types de zones de liste, données ne sont pas écrite à l’interface de la propriété. 
  
Uniquement les propriétés de type chaîne à valeurs multiples sont pris en charge pour la liste déroulante à valeurs multiples ; autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

