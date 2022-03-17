---
title: PaperSource, cellule (section PrintProperties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
ms.localizationpriority: medium
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Détermine la source de papier pour la page.
ms.openlocfilehash: 320efcc2efa82d8d88a081d0feed1a8b389ef07e
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520552"
---
# <a name="papersource-cell-printproperties-section"></a>PaperSource, cellule (section PrintProperties)

Détermine la source de papier pour la page. 
  
## <a name="remarks"></a>Remarques

Ce paramètre correspond au paramètre **Source** de la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis, sous l’onglet **Configuration**, cliquez sur le bouton **Configuration**).
  
Les valeurs numériques de cette cellule sont mélisées sur des constantes (préfixées par DMBIN) définies pour les sélections bin dans le fichier wingdi.h de Microsoft Windows ; par exemple, la valeur 7 représente DMBIN_AUTO. 
  
Pour obtenir une référence à la cellule PaperSource par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |PaperSource  <br/> |
   
Pour obtenir une référence à la cellule PaperSource à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
|**Index de la cellule :**  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

