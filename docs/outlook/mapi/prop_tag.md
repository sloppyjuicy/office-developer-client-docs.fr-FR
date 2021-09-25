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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e1d1f759989ae7c241317b7488ce0d8f53180e9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609634"
---
# <a name="prop_tag"></a>PROP_TAG

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une balise de propriété créée en combinant un type de propriété et un identificateur spécifiés. 
  
|||
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

La macro **\_ PROP TAG** crée une balise de propriété pour une propriété de type  _ulPropType_ et l’identificateur spécifié dans  _ulPropID_. Par exemple, une balise de propriété pour un identificateur d’entrée peut être créée à l’aide de la macro **PROP_TAG** comme suit : 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Les 16 bits de bas ordre de la balise de propriété renvoyée contiennent le type de propriété, PT_BINARY et les 16 bits de haut niveau contiennent l’identificateur de propriété, 0xFFFF.
  
Pour plus d’informations sur les balises de propriété, voir [MAPI Property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [Macros liées aux structures](macros-related-to-structures.md)

