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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439701"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste à plusieurs valeurs qui s'affiche dans une boîte de dialogue créée à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> MSR doit être égal à zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVLISTBOX** décrit une liste à plusieurs valeurs standard qui contient une liste d'éléments en lecture seule. À l'aide d'une liste à plusieurs valeurs standard, les valeurs s'affichent immédiatement. 
  
Les données affichées proviennent de la propriété identifiée dans le membre **ulMVPropTag** . Il n'existe aucun besoin de lire à partir de l'interface de propriétés associée à la table d'affichage. En outre, étant donné que les utilisateurs ne peuvent pas effectuer des sélections à partir de ces types de listes, les données ne sont pas écrites dans l'interface de propriété. 
  
Seules les propriétés de chaîne à valeurs multiples sont prises en charge pour la liste à valeurs multiples; les autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

