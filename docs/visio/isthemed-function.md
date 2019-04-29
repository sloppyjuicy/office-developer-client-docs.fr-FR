---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Renvoie une valeur de type Boolean qui indique si un thème est appliqué à une forme.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418119"
---
# <a name="isthemed-function"></a>Fonction ISTHEMED

Renvoie une valeur de type Boolean qui indique si un thème est appliqué à une forme. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **ISTHEMED** ()
  
## <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

> [!NOTE]
> La fonction **ISTHEMED** dans Visio 2013 remplace la fonction **CELLISTHEMED** des versions précédentes de Visio. 
  
La fonction **ISTHEMED** vous permet d'affecter des parties appropriées de la mise en forme d'un thème à une forme, tout en conservant la possibilité de remplacer les autres parties de la mise en forme de thème par une mise en forme manuelle. Si, par la suite, vous réappliquez le thème, toute mise en forme manuelle est remplacée et la forme prend la mise en forme du thème. 
  
 **ISTHEMED** renvoie la valeur true si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0. Si cette cellule est égale à 0, **ISTHEMED** prend la valeur false. Le thème de DocumentSheet et PageSheet n'affecte pas la valeur de la fonction **ISTHEMED** utilisée dans une feuille ShapeSheet. Uniquement si la fonction **ISTHEMED** s'affiche dans la PageSheet fait le thème de la page. 
  
## <a name="example"></a>Exemple

||||
|:-----|:-----|:-----|
|Cell  <br/> |Formule  <br/> |Résultat  <br/> |
|Char. font  <br/> |IF (ISTHEMED (), THEMEVAL (), FONT ("Calibri"))  <br/> |Si des thèmes sont appliqués à la forme, le texte de la forme accepte la mise en forme de la police du thème. Si la forme n'est pas à thème, le texte de la forme est mis en forme avec la police «Calibri».  <br/> |
|LineColor  <br/> |SI (ISTHEMED, RGB (255, 0, 0), RVB (0, 255, 0))  <br/> |Si des thèmes sont appliqués à la forme, la couleur de trait de la forme est rouge. Si la forme n'est pas à thème, la couleur de trait de la forme est verte.  <br/> |
   

