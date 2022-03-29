---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: Renvoie une balise de propriété créée en combinant un type de propriété spécifié et un identificateur pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 3d82f00c92ed750ea5c1189890d2be6e85524c5f
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456300"
---
# <a name="prop_tag"></a>PROP_TAG

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une balise de propriété créée en combinant un type de propriété et un identificateur spécifiés. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Paramètres

_ulPropType_
  
> Type de propriété pour la nouvelle balise de propriété.
    
_ulPropID_
  
> Identificateur de propriété pour la nouvelle balise de propriété.
    
## <a name="remarks"></a>Remarques

La macro **PROPTAG\_** crée une balise de propriété pour une propriété de type _ulPropType_ et l’identificateur spécifié dans _ulPropID_. Par exemple, une balise de propriété pour un identificateur d’entrée peut être créée à l’aide de **la macro PROP_TAG** comme suit : 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Les 16 bits de bas ordre de la balise de propriété renvoyée contiennent le type de propriété, PT_BINARY et les 16 bits de haut niveau contiennent l’identificateur de propriété, 0xFFFF.
  
Pour plus d’informations sur les balises de propriété, voir [MAPI Property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [Macros liées aux structures](macros-related-to-structures.md)

