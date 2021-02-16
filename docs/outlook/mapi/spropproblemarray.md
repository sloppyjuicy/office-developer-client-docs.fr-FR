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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406856"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau d’une ou plusieurs structures [SPropProblem.](spropproblem.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> Nombre de structures [SPropProblem](spropproblem.md) dans le tableau indiqué par le **membre aProblem.** 
    
 **aProblem**
  
> Tableau de structures **SPropProblem,** chacune décrivant une erreur de propriété. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur le fonctionnement des structures **SPropProblem** et **SPropProblemArray** avec les erreurs liées aux propriétés, voir PROPRIÉTÉS nommées [MAPI.](mapi-named-properties.md) 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Structures MAPI](mapi-structures.md)

