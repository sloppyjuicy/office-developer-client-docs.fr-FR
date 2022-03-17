---
title: PaperKind, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
ms.localizationpriority: medium
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Indique le type de papier sur lequel imprimer la page.
ms.openlocfilehash: 17431a4175ba804c3a7d213aaeda29662536b3e2
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520559"
---
# <a name="paperkind-cell-print-properties-section"></a>PaperKind, cellule (section Print Properties)

Indique le type de papier sur lequel imprimer la page.
  
## <a name="remarks"></a>Remarques

Ce paramètre correspond au paramètre Taille  du papier de la boîte  de dialogue Configuration de l’impression  (sous l’onglet Création, cliquez sur la flèche Mise en  **page**, puis sous l’onglet Configuration de l’impression, cliquez sur le bouton Installation). 
  
Les valeurs numériques de cette cellule sont m mappés à des constantes (préfixées par DMPAPER) définies pour les sélections de papier dans le fichier wingdi.h de Microsoft Windows. 
  
Pour obtenir une référence à la cellule PaperKind par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |PaperKind  <br/> |
   
Pour obtenir une référence à la cellule PaperKind à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
|**Index de la cellule :**  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

