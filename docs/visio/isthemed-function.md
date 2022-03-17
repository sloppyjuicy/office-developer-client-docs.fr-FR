---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Cette propriété renvoie une valeur de booléen indiquant si un thème est appliqué à une forme.
ms.openlocfilehash: 8fe04b262dad8e1008763d34e9b1407de0c558bc
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520853"
---
# <a name="isthemed-function"></a>Fonction ISTHEMED

Cette propriété renvoie une valeur de booléen indiquant si un thème est appliqué à une forme. 
  
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
  
 **ISTHEMED** prend la valeur TRUE si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0. Si cette cellule est égale à 0, **ISTHEMED** a la valeur FALSE. Le thème de la feuille de document et de la feuille page n’affecte pas la valeur de la **fonction ISTHEMED** utilisée dans une feuille ShapeSheet. Le thème de la page n’a d’importance que si la fonction **ISTHEMED** s’affiche dans la feuille de page. 
  
## <a name="example"></a>Exemple

|Cell  <br/> |Formule  <br/> |Résultat  <br/> |
|:-----|:-----|:-----|
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT(« Calibri »))  <br/> |Si un thème est appliqué à la forme, le texte de la forme accepte la mise en forme de police du thème. Si la forme n’est pas un modèle, le texte de la forme est formaté avec la police « Calibri ». |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Si un themed est appliqué à la forme, la couleur de trait de la forme est rouge. Si la forme n’est pas sur le themed, la couleur de trait de la forme est verte. |
   

