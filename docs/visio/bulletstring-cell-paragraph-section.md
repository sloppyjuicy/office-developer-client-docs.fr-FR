---
title: BulletString, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permet de créer un style de puce personnalisé.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788194"
---
# <a name="bulletstring-cell-paragraph-section"></a>BulletString, cellule (section Paragraph)

Permet de créer un style de puce personnalisé. 
  
## <a name="remarks"></a>Remarques

Entrez le style sous la forme d’une chaîne (entre guillemets). Par exemple, entrez la chaîne « ooo ».
  
Vous pouvez également définir la valeur de cette cellule en cliquant sur une forme, en pointant sur **Format**, en cliquant sur **texte**, puis en cliquant sur l’onglet **puces** . 
  
Pour obtenir une référence à la cellule BulletString par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Para.BulletStr [ *i* ] où *i* = < 1 >, 2, 3,...  <br/> |
   
Pour obtenir une référence à la cellule BulletString par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionParagraph** <br/> |
|Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visBulletString** <br/> |
   

