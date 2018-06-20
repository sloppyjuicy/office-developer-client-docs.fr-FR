---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787191"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**S’applique à**: Outlook 
  
Crée une structure [SSortOrderSet](ssortorderset.md) nommée qui contient un nombre spécifié d’ordres de tri. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Paramètres

__csort_
  
> Nombre d’ordres de tri à inclure dans la nouvelle structure.
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSSortOrderSet** pour créer un ordre de tri avec des limites explicites. 
  
Pour utiliser la nouvelle structure de résultats de la macro **SizedSSortOrderSet** comme un pointeur vers une structure **SSortOrderSet** , effectuer le cast suivant : 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Voir aussi

- [SSortOrderSet](ssortorderset.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

