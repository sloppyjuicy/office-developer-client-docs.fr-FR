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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cbead0a9953ae5106e1fcc7d07d965d4dc7bacb9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570988"
---
# <a name="proptag"></a>PROP_TAG

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie une balise de propriété créée en combinant un identificateur et le type de propriété spécifié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Paramètres

_ulPropType_
  
> Type de propriété de la nouvelle balise de propriété.
    
_ulPropID_
  
> Identificateur de la propriété de la nouvelle balise de propriété.
    
## <a name="remarks"></a>Remarques

Le **propriétés\_balise** macro crée une balise de propriété pour une propriété de type _ulPropType_ et l’identificateur est spécifié dans _ulPropID_. Par exemple, une balise de propriété pour un identificateur d’entrée peut être créée à l’aide de la macro **PROP_TAG** comme suit : 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Les 16 bits de poids faible de la balise de propriété renvoyée contient le type de propriété PT_BINARY, et les 16 bits de poids fort contient l’identificateur de la propriété 0xFFFF.
  
Pour plus d’informations sur les balises de propriété, voir [Balises de propriété MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [Macros liées aux structures](macros-related-to-structures.md)

