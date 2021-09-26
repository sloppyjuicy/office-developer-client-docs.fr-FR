---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Renvoie une valeur de booléen indiquant si un thème est appliqué à une forme.
ms.openlocfilehash: 56fdbe781f8178bc7a388ff2d0540b8d3f0c1dc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612567"
---
# <a name="isthemed-function"></a>Fonction ISTHEMED

Renvoie une valeur de booléen indiquant si un thème est appliqué à une forme. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **ISTHEMED**()
  
## <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

> [!NOTE]
> La **fonction ISTHEMED** dans Visio 2013 remplace la fonction **CELLISTHEMED** des versions précédentes de Visio. 
  
La **fonction ISTHEMED** vous permet d’affecter des parties appropriées de la mise en forme d’un thème à une forme, tout en conservant la possibilité de remplacer d’autres parties de la mise en forme de thème par une mise en forme appliquée manuellement. Si, par la suite, vous réappliquez le thème, toute mise en forme manuelle est mise en forme et la forme prend l’ensemble de la mise en forme du thème. 
  
 **ISTHEMED** est évalué à TRUE si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0. Si cette cellule est égale à 0, **ISTHEMED** est évalué à FALSE. Le thème de la feuille de document et de la feuille page n’affecte pas la valeur de la **fonction ISTHEMED** utilisée dans une feuille ShapeSheet. Le thème de la page n’a d’importance que si la fonction **ISTHEMED** s’affiche dans la feuille de page. 
  
## <a name="example"></a>Exemple

||||
|:-----|:-----|:-----|
|Cell  <br/> |Formule  <br/> |Résultat  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT(« Calibri »))  <br/> |Si un thème est appliqué à la forme, le texte de la forme accepte la mise en forme de police du thème. Si la forme n’est pas sur le modèle, le texte de la forme est formaté avec la police « Calibri ».  <br/> |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Si un themed est appliqué à la forme, la couleur de trait de la forme est rouge. Si la forme n’est pas sur le themed, la couleur de trait de la forme est vert.  <br/> |
   

