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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572563"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
- [Macros liées aux structures](macros-related-to-structures.md)

