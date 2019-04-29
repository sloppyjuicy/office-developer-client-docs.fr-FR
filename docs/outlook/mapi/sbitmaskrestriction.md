---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424475"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de masque de bits, qui est utilisée pour **** effectuer une opération and au niveau du bit et tester le résultat. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>Members

 **relBMR**
  
> Opérateur relationnel qui décrit comment le masque spécifié dans le membre **ulMask** doit être appliqué à la balise de propriété. Les valeurs possibles sont les suivantes: 
    
BMR_EQZ 
  
> Effectuer une opération **** and au niveau du bit du masque dans le membre **ulMask** avec la propriété représentée par le membre **ulPropTag** et vérifier qu'il est égal à zéro. 
    
BMR_NEZ 
  
> Effectuer une opération **** and au niveau du bit du masque dans le membre **ulMask** avec la propriété représentée par le membre **ulPropTag** et vérifier qu'elle n'est pas égale à zéro. 
    
 **ulPropTag**
  
> Balise de propriété de la propriété à laquelle le masque de masque est appliqué.
    
 **ulMask**
  
> Masque de à appliquer à la propriété identifiée par **ulPropTag**.
    
## <a name="remarks"></a>Remarques

La structure **SBitMaskRestriction** effectue une opération de bits **and** à l'aide du masque de bits décrit dans le membre **ulMask** et de la valeur de la propriété décrite par le membre **ulPropTag** . Si le résultat est égal à zéro, BMR_EQZ est satisfait. S'il est différent de zéro, autrement dit, si la valeur de la propriété a au moins un des mêmes bits défini comme **ulMask**, BMR_NEZ est satisfait.
  
Pour plus d'informations sur la structure **SBitMaskRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

