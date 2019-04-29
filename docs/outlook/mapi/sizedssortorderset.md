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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428605"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [SSortOrderSet](ssortorderset.md) nommée qui contient un nombre spécifié d'ordres de tri. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Structure associée:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Paramètres

__csort_
  
> Nombre d'ordres de tri à inclure dans la nouvelle structure.
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSSortOrderSet** pour créer un ensemble d'ordres de tri avec des limites explicites. 
  
Pour utiliser la nouvelle structure qui résulte de la macro **SizedSSortOrderSet** en tant que pointeur vers une structure **SSortOrderSet** , effectuez la conversion suivante: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Voir aussi

- [SSortOrderSet](ssortorderset.md)
- [Macros liées aux structures](macros-related-to-structures.md)

