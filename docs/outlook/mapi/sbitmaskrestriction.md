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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787050"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**S’applique à**: Outlook 
  
Décrit une restriction de masque de bits, qui est utilisée pour effectuer une opération de bits **AND** et tester le résultat. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>Membres

 **relBMR**
  
> Opérateur de relation qui décrit comment le masque spécifié dans le membre **ulMask** doit être appliqué à la balise de propriété. Les valeurs possibles sont les suivantes : 
    
BMR_EQZ 
  
> Effectuer une opération de bits **AND** du masque dans le membre **ulMask** avec la propriété représentée par les membres **ulPropTag** et le test pour être égale à zéro. 
    
BMR_NEZ 
  
> Exécuter une opération **et** du masque dans le membre **ulMask** avec la propriété représentée par le membre **ulPropTag** et testez n’étant ne pas égal à zéro. 
    
 **ulPropTag**
  
> Balise de propriété de la propriété à laquelle s’applique le masque de bits.
    
 **ulMask**
  
> Masque de bits à appliquer à la propriété identifiée par **ulPropTag**.
    
## <a name="remarks"></a>Remarques

La structure **SBitMaskRestriction** effectue une opération de bits **AND** à l’aide de masque de bits décrite dans le membre **ulMask** et la valeur de la propriété définie par le membre **ulPropTag** . Si le résultat est égale à zéro, BMR_EQZ est remplie. Si elle est différente de zéro, autrement dit, si la valeur de propriété comporte au moins un des bits même définir en tant **ulMask**, puis BMR_NEZ est satisfaite.
  
Pour plus d’informations sur les restrictions de structure **SBitMaskRestriction** en général, voir [à propos des Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

