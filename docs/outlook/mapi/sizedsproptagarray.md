---
title: SizedSPropTagArray
description: Décrit SizedSPropTagArray, qui crée une structure nommée SPropTagArray qui inclut un nombre spécifié de balises de propriété.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
ms.openlocfilehash: 5b450aa875ba0b44db82ef3e244388aeeca59283
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894095"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [nommée SPropTagArray](sproptagarray.md) qui inclut un nombre spécifié de balises de propriété. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure associée :  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Paramètres

_ _ctag_
  
> Nombre de balises de propriété à inclure dans la nouvelle structure.
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSPropTagArray** pour créer un tableau de balises de propriétés avec des limites explicites. 
  
Pour utiliser la nouvelle structure qui résulte de la macro **SizedSPropTagArray** comme pointeur vers une structure **SPropTagArray** , effectuez le cast suivant : 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Voir aussi

- [SPropTagArray](sproptagarray.md)
- [Macros liées aux structures](macros-related-to-structures.md)

