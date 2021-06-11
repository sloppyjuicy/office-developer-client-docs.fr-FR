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
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408445"
---
# <a name="paperkind-cell-print-properties-section"></a>PaperKind, cellule (section Print Properties)

Indique le type de papier sur lequel imprimer la page.
  
## <a name="remarks"></a>Remarques

Ce paramètre correspond au paramètre Taille du papier de  la boîte de dialogue Configuration de l’impression (sous  l’onglet Création, cliquez sur la flèche Mise en **page,** puis sous l’onglet Configuration de l’impression, cliquez sur le bouton Installation).    
  
Les valeurs numériques de cette cellule sont m mappés à des constantes (préfixées par DMPAPER) définies pour les sélections de papier dans le fichier wingdi.h de Microsoft Windows. 
  
Pour obtenir une référence à la cellule PaperKind par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PaperKind  <br/> |
   
Pour obtenir une référence à la cellule PaperKind à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

