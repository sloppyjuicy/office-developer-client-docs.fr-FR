---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 384282445e6f50fac3d440e4df3a4c8e61e0c8a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551666"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste liste liste qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.
  
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

## <a name="members"></a>Membres

 **ulFlags**
  
> Réservé ; doit être zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING. Les différentes valeurs de cette propriété sont affichées sous forme d’entrées distinctes dans la liste de listes.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVDDLBOX** décrit une liste de listes à valeurs multiples, une liste d’éléments en lecture seule. À l’aide d’une liste finale à valeurs multiples, les valeurs sont affichées lorsqu’un utilisateur clique sur une barre de défilement. 
  
Les données affichées proviennent de la propriété identifiée dans le **membre ulMVPropTag.** Il n’est pas nécessaire de lire l’interface de propriétés associée au tableau d’affichage. En outre, étant donné que les utilisateurs ne sont pas en mesure d’effectuer des sélections à partir de ces types de zones de liste, les données ne sont pas écrites dans l’interface des propriétés. 
  
Seules les propriétés de chaîne à valeurs multiples sont pris en charge pour la liste de listes listes à valeurs multiples ; les autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

