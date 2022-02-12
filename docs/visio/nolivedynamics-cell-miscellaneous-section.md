---
title: NoLiveDynamics, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
ms.localizationpriority: medium
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Détermine si une forme est redimensionnée ou pivote de façon dynamique lorsque vous la manipulez.
ms.openlocfilehash: c74440fc37b4d47557992ac8c7df06a935d2916b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62786100"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>NoLiveDynamics, cellule (section Miscellaneous)

Détermine si une forme est redimensionnée ou pivote de façon dynamique lorsque vous la manipulez.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme n'est pas mise à jour dynamiquement lorsque vous la manipulez. |
| FALSE  <br/> | La forme est mise à jour dynamiquement lorsque vous la manipulez. |
   
## <a name="remarks"></a>Remarques

Lorsque vous redimensionnez ou faites pivoter une forme 2D sans effets dynamiques, un rectangle de sélection s'affiche. S'il s'agit d'une forme 1D, le retour visuel est basé sur la valeur de la cellule DynFeedback.
  
Pour obtenir une référence à la cellule NoLiveDynamics par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | NoLiveDynamics  <br/> |
   
Pour obtenir une référence à la cellule NoLiveDynamics à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section  :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visNoLiveDynamics** <br/> |
   

