---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787243"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau d’une ou plusieurs structures [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Membres

 **cProblem**
  
> Nombre de structures [SPropProblem](spropproblem.md) dans le tableau indiqué par le membre **aProblem** . 
    
 **aProblem**
  
> Tableau de structures **SPropProblem** , décrivant chacun une erreur de propriété. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur le fonctionnement des structures **SPropProblem** et **SPropProblemArray** avec des erreurs liées aux propriétés, voir [Les propriétés MAPI nommée](mapi-named-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Structures MAPI](mapi-structures.md)

