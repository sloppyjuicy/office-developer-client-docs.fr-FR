---
title: HideForApply, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Détermine où un style apparaît dans l’interface utilisateur de Microsoft Visio.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788787"
---
# <a name="hideforapply-cell-style-properties-section"></a>HideForApply, cellule (section Style Properties)

Détermine où un style apparaît dans l’interface utilisateur de Microsoft Visio.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le style apparaît uniquement dans l' **Explorateur de dessins**.  <br/> |
| FALSE  <br/> | Le style apparaît dans l' **Explorateur de dessins**.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous basez un nouveau style sur un style masqué, il n'hérite pas de cet attribut.
  
Pour obtenir une référence à la cellule HideForApply par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | HideForApply  <br/> |
   
Pour obtenir une référence à la cellule HideForApply par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowStyle** <br/> |
| Index de la cellule :  <br/> |**visStyleHidden** <br/> |
   

