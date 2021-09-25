---
title: HideForApply, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
ms.localizationpriority: medium
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Détermine l’endroit où un style est affiché dans l’interface utilisateur Visio Microsoft.
ms.openlocfilehash: 18750f8191d468483b63f7e076ada1b4cd2072f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570490"
---
# <a name="hideforapply-cell-style-properties-section"></a>HideForApply, cellule (section Style Properties)

Détermine l’endroit où un style est affiché dans l’interface utilisateur Visio Microsoft.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le style n’apparaît que dans l’**Explorateur de dessins**.  <br/> |
| FALSE  <br/> | Le style apparaît dans l’**Explorateur de dessins**.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous basez un nouveau style sur un style masqué, il n'hérite pas de cet attribut.
  
Pour obtenir une référence à la cellule HideForApply par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | HideForApply  <br/> |
   
Pour obtenir une référence à la cellule HideForApply à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowStyle** <br/> |
| Index de la cellule :  <br/> |**visStyleHidden** <br/> |
   

