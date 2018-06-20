---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Renvoie une valeur Boolean indiquant si une forme possède un thème est appliqué.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788892"
---
# <a name="isthemed-function"></a>Fonction ISTHEMED

Renvoie une valeur Boolean indiquant si une forme possède un thème est appliqué. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013 
  
## <a name="syntax"></a>Syntaxe

 **ISTHEMED** ()
  
## <a name="return-value"></a>Valeur renvoy�e

Booléenne
  
## <a name="remarks"></a>Remarques

> [!NOTE]
> La fonction **ISTHEMED** dans Visio 2013 remplace la fonction **CELLISTHEMED** à partir de versions antérieures de Visio. 
  
**ISTHEMED** permet d’affecter les aspects de la mise en forme d’un thème à une forme de fonction tout en conservant la possibilité de remplacer les autres composants du thème de la mise en forme appliquée manuellement la mise en forme. Si vous réappliquez ensuite le thème, toute mise en forme manuelle est remplacé et toute la mise en forme du thème prend la forme. 
  
 **ISTHEMED** renvoie la valeur TRUE si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0. Si cette cellule est égale à 0, **ISTHEMED** a la valeur FALSE. Le thème de la propriété DocumentSheet et PageSheet n’affecte pas la valeur de la fonction **ISTHEMED** utilisée dans une feuille ShapeSheet. Uniquement si la fonction **ISTHEMED** s’affiche dans le PageSheet n’en matière de thème de la page. 
  
## <a name="example"></a>Exemple

||||
|:-----|:-----|:-----|
|Cellule  <br/> |Formule  <br/> |Résultat  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Si la forme possède un thème appliqué, le texte de la forme accepte la mise en forme du thème de police. Si la forme n’est pas à thème, le texte de la forme est mise en forme avec la police « Calibri ».  <br/> |
|LineColor  <br/> |IF (ISTHEMED, RVB (255, 0, 0), RVB (0, 255, 0))  <br/> |Si la forme possède un thème appliqué, la couleur de trait de la forme est rouge. Si la forme n’est pas à thème, la couleur de trait de la forme est verte.  <br/> |
   

