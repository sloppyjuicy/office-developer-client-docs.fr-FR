---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aee62a1cce88d606231acd67f3b0ec7f8e3bdbf2
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634575"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste à valeurs multiples qui sera affichée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> Réservé ; doit être zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVLISTBOX** décrit une liste à valeurs multiples standard avec une liste d’éléments en lecture seule. À l’aide d’une liste à valeurs multiples standard, les valeurs sont affichées immédiatement. 
  
Les données affichées proviennent de la propriété identifiée dans le **membre ulMVPropTag** . Il n’est pas nécessaire de lire l’interface de propriétés associée au tableau d’affichage. En outre, étant donné que les utilisateurs ne sont pas en mesure d’effectuer des sélections à partir de ces types de listes, les données ne sont pas écrites dans l’interface des propriétés. 
  
Seules les propriétés de chaîne à valeurs multiples sont pris en charge pour la liste à valeurs multiples ; les autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Consultez aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

