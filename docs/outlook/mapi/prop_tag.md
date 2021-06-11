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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425882"
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

## <a name="parameters"></a>Parameters

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

