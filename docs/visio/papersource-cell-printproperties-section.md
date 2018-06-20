---
title: PaperSource, cellule (section PrintProperties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Détermine la source de papier pour la page.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789216"
---
# <a name="papersource-cell-printproperties-section"></a>PaperSource, cellule (section PrintProperties)

Détermine la source de papier pour la page. 
  
## <a name="remarks"></a>Remarques

Ce paramètre correspond au paramètre **d’Alimentation papier** dans la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** et cliquez sur l’onglet **Configuration de l’impression** , **le programme d’installation**).
  
Les valeurs numériques de cette cellule correspondent à des constantes (ayant pour préfixe DMBIN) définies pour les sélections de Corbeille dans le fichier wingdi.h de Microsoft Windows ; par exemple, la valeur 7 représente DMBIN_AUTO. 
  
Pour obtenir une référence à la cellule PaperSource par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PaperSource  <br/> |
   
Pour obtenir une référence à la cellule PaperSource par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

