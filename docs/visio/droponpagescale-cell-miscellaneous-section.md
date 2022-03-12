---
title: DropOnPageScale, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
ms.localizationpriority: medium
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 81bcb4432fdff3e7131291cfa74bf66d77bd66cc
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63447633"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>DropOnPageScale, cellule (section Miscellaneous)

Contient le pourcentage auquel une forme est mise à l'échelle lorsqu'elle est glissée sur la page de dessin.
  
## <a name="remarks"></a>Remarques

Dans les deux cas suivants, Visio met à l'échelle les formes pour qu'elles apparaissent correctement sur la page de dessin :
  
- lorsque des formes non mesurées sont glissées sur des dessins mis à l'échelle ;
    
- Lorsque les formes mesurées sont déposés sur des dessins non retentés.
    
Le pourcentage dans la cellule DropOnPageScale indique le facteur selon lequel Visio mise à l’échelle de la forme, soit vers le haut (\>100) soit vers le bas (\<100). Vous pouvez utiliser ce nombre comme facteur lorsque vous calculez des valeurs préprogrammées. 
  
Cette valeur est de 100 % pour les formes mesurées sur des dessins mis à l'échelle ou les formes non mesurées sur des dessins non mis à l'échelle. 
  
Pour obtenir une référence à la cellule DropOnPageScale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | DropOnPageScale  <br/> |
   
Pour obtenir une référence à la cellule DropOnPageScale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowMisc** <br/> |
| **Index de la cellule :**  <br/> |**visObjDropOnPageScale** <br/> |
   

