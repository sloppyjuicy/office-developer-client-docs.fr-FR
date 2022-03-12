---
title: BulletString, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
ms.localizationpriority: medium
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permet de créer un style de puce personnalisé.
ms.openlocfilehash: e05d477c6cb3ed3dcbb9948f28cbbe50f947f482
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448453"
---
# <a name="bulletstring-cell-paragraph-section"></a>BulletString, cellule (section Paragraph)

Permet de créer un style de puce personnalisé. 
  
## <a name="remarks"></a>Remarques

Entrez le style sous la forme d’une chaîne (entre guillemets). Par exemple, entrez la chaîne « ooo ».
  
Vous pouvez également définir la valeur de cette cellule en cliquant avec le bouton droit sur une forme, en pointant sur **Format**, en cliquant sur **Texte**, puis en cliquant sur l’onglet **Puces**. 
  
Pour obtenir une référence à la cellule BulletString par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Para.BulletStr[ *i*  ] où  *i*  = <1>, 2, 3, ... |
   
Pour obtenir une référence à la cellule BulletString à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionParagraph** <br/> |
|**Index de la ligne :**  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2, ... |
|**Index de la cellule :**  <br/> |**visBulletString** <br/> |
   

