---
title: DTBLMVLISTBOX
description: DTBLMVLISTBOX décrit une liste à valeurs multiples qui s’affiche dans une boîte de dialogue générée à partir d’une table d’affichage.
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
ms.openlocfilehash: 35aaf93c4a39fbd7fdfc23fb61c91f51d1d07739
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818228"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste à valeurs multiples qui s’affiche dans une boîte de dialogue créée à partir d’une table d’affichage.
  
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
  
> Réservé; doit être égal à zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVLISTBOX** décrit une liste à valeurs multiples standard qui a une liste d’éléments en lecture seule. À l’aide d’une liste à valeurs multiples standard, les valeurs sont affichées immédiatement. 
  
Les données affichées proviennent de la propriété identifiée dans le membre **ulMVPropTag** . Il n’est pas nécessaire de lire à partir de l’interface de propriété associée à la table d’affichage. En outre, étant donné que les utilisateurs ne sont pas en mesure d’effectuer des sélections à partir de ces types de listes, les données ne sont pas écrites dans l’interface de propriété. 
  
Seules les propriétés de chaîne à valeurs multiples sont prises en charge pour la liste à valeurs multiples ; d’autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

