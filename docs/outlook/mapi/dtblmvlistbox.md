---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f7c1241f2ad31dee8277f3b3b77ac02137067a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576308"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une liste à valeurs multiples qui s’affichera dans la boîte de dialogue qui est générée à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Réservé ; doit être égal à zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVLISTBOX** décrit une liste à valeurs multiples standard qui comporte une liste en lecture seule d’éléments. En utilisant une liste à valeurs multiples standard, les valeurs sont affichées immédiatement. 
  
Les données qui sont affichées provient de la propriété identifiée dans le membre **ulMVPropTag** . Il n’existe aucune exigence pour lire à partir de l’interface de la propriété qui est associé à la table d’affichage. En outre, étant donné que les utilisateurs ne sont pas en mesure de réaliser des sélections à partir de ces types de listes, données ne sont pas écrite à l’interface de la propriété. 
  
Uniquement les propriétés de type chaîne à valeurs multiples sont pris en charge pour la liste à valeurs multiples ; autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

