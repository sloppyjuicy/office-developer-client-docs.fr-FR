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
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357840"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau d'une ou de plusieurs structures [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> Nombre de structures [SPropProblem](spropproblem.md) dans le tableau indiqué par le membre **aProblem** . 
    
 **aProblem**
  
> Tableau de structures **SPropProblem** , qui décrivent chacune une erreur de propriété. 
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur la façon dont les structures **SPropProblem** et **SPropProblemArray** fonctionnent avec les erreurs liées aux propriétés, voir [MAPI named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Structures MAPI](mapi-structures.md)

