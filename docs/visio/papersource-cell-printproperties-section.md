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
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301462"
---
# <a name="papersource-cell-printproperties-section"></a>PaperSource, cellule (section PrintProperties)

Détermine la source de papier pour la page. 
  
## <a name="remarks"></a>Remarques

Ce paramètre correspond au paramètre **Source** de la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis, sous l’onglet **Configuration**, cliquez sur le bouton **Configuration**).
  
Les valeurs numériques de cette cellule correspondent aux constantes (portant le préfixe DMBIN) définies pour les sélections d'emplacement dans le fichier Microsoft Windows WinGDI. h; par exemple, la valeur 7 représente DMBIN_AUTO. 
  
Pour obtenir une référence à la cellule PaperSource par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PaperSource  <br/> |
   
Pour obtenir une référence à la cellule PaperSource à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

