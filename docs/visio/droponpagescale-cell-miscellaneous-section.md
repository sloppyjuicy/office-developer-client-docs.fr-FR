---
title: DropOnPageScale, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788518"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>DropOnPageScale, cellule (section Miscellaneous)

Contient le pourcentage auquel une forme est mise à l'échelle lorsqu'elle est glissée sur la page de dessin.
  
## <a name="remarks"></a>Note

Dans les deux cas suivants, Visio met à l'échelle les formes pour qu'elles apparaissent correctement sur la page de dessin :
  
- lorsque des formes non mesurées sont glissées sur des dessins mis à l'échelle ;
    
- Lorsque des formes mesurées sont glissées sur des dessins.
    
Le pourcentage de la cellule DropOnPageScale indique le facteur par lequel Visio à l’échelle de la forme, haut (\>100) ou vers le bas (\<100). Vous pouvez utiliser ce numéro comme un facteur lors du calcul des valeurs codées en dur. 
  
Cette valeur est de 100 % pour les formes mesurées sur des dessins mis à l'échelle ou les formes non mesurées sur des dessins non mis à l'échelle. 
  
Pour obtenir une référence à la cellule DropOnPageScale par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DropOnPageScale  <br/> |
   
Pour obtenir une référence à la cellule DropOnPageScale par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visObjDropOnPageScale** <br/> |
   

