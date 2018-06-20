---
title: PaperKind, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Indique le type de papier sur lequel imprimer la page.
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789220"
---
# <a name="paperkind-cell-print-properties-section"></a>PaperKind, cellule (section Print Properties)

Indique le type de papier sur lequel imprimer la page.
  
## <a name="remarks"></a>Remarques

Ce paramètre correspond au paramètre de **Taille de papier** dans la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis, sous l’onglet **Configuration de l’impression** , cliquez sur le bouton de **l’installation** ). 
  
Les valeurs numériques de cette cellule correspondent à des constantes (ayant pour préfixe DMPAPER) définies pour les sélections de papier dans le fichier wingdi.h de Microsoft Windows. 
  
Pour obtenir une référence à la cellule PaperKind par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PaperKind  <br/> |
   
Pour obtenir une référence à la cellule PaperKind par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

