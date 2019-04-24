---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328566"
---
# <a name="proptag"></a>PROP_TAG

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une balise de propriété créée en combinant un type et un identificateur de propriété spécifiés. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Structure associée:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Paramètres

_ulPropType_
  
> Type de propriété de la nouvelle balise de propriété.
    
_ulPropID_
  
> Identificateur de propriété de la nouvelle balise de propriété.
    
## <a name="remarks"></a>Remarques

La macro de **baliSe\_prop** crée une balise de propriété pour une propriété de type _ulPropType_ et l'identificateur qui est spécifié dans _ulPropID_. Par exemple, une balise de propriété pour un identificateur d'entrée peut être créée à l'aide de la macro **PROP_TAG** comme suit: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Les 16 bits de poids faible de la balise de propriété renvoyée contiennent le type de propriété PT_BINARY et les bits de poids fort 16 contiennent l'identificateur de propriété 0xFFFF.
  
Pour plus d'informations sur les balises de propriété, voir [MAPI Property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [Macros liées aux structures](macros-related-to-structures.md)

