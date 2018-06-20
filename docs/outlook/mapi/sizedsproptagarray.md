---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787176"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**S’applique à**: Outlook 
  
Crée une structure [SPropTagArray](sproptagarray.md) nommée qui inclut un nombre spécifié de balises de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Paramètres

__ctag_
  
> Nombre de balises de propriétés à inclure dans la nouvelle structure.
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSPropTagArray** pour créer un tableau de balise de propriété avec des limites explicites. 
  
Pour utiliser la nouvelle structure de résultats de la macro **SizedSPropTagArray** comme un pointeur vers une structure **SPropTagArray** , effectuer le cast suivant : 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Voir aussi

- [SPropTagArray](sproptagarray.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

