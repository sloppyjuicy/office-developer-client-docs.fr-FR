---
title: SizedSPropTagArray
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7bf7d23b9478810b036639396b7c29dfad1b412d
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63713500"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [nommée SPropTagArray](sproptagarray.md) qui inclut un nombre spécifié de balises de propriété. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Paramètres

_ _ctag_
  
> Nombre de balises de propriété à inclure dans la nouvelle structure.
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSPropTagArray pour créer** un tableau de balises de propriétés avec des limites explicites. 
  
Pour utiliser la nouvelle structure qui résulte de la macro **SizedSPropTagArray** comme pointeur vers une structure **SPropTagArray** , effectuez la distribution suivante : 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Voir aussi

- [SPropTagArray](sproptagarray.md)
- [Macros liées aux structures](macros-related-to-structures.md)

