---
title: À propos des valeurs d'erreur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Des valeurs d'erreur s'affichent dans les cellules contenant une formule incorrecte.
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787975"
---
# <a name="about-error-values"></a>À propos des valeurs d'erreur

Des valeurs d'erreur s'affichent dans les cellules contenant une formule incorrecte.
  
Si une formule fait référence à une cellule qui contient une valeur d'erreur, elle affiche également une valeur d'erreur. Utilisez les fonctions ISERR, ISERRNA, ISERROR ou ISERRVALUE pour déterminer le sens de ces valeurs d'erreur.
  
**Valeurs d’erreur**

||||
|:-----|:-----|:-----|
|**Si la cellule affiche** <br/> |**La formule contient** <br/> |**Exemple** <br/> |
| #DIV/0!  <br/> |Division par 0  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Un argument ou un opérande de type incorrect  <br/> | 5 + « Maison »  <br/> |
| #REF!  <br/> | Une référence à une cellule qui n’existe pas  <br/> | Une cellule qui fait référence à une cellule qui n’existe plus  <br/> |
| #NUM!  <br/> | Un nombre non valide  <br/> | Racine carrée d’un nombre négatif  <br/> |
| #N/A!  <br/> | Pas une valeur disponible  <br/> | Fonction NA)  <br/> |
| #DIM !  <br/> | Une valeur de cote qui dépasse la plage autorisée (les puissances correctes sont des entiers -128 \<= n \<= 127)  <br/> Une valeur de cote utilisée avec une opération non appropriée  <br/> |1 en ^ 100 \* 1 en ^ 100 (le résultat est 1 dans ^ 200, qui dépasse la plage des cotes)  <br/> 5,2 cm ^ 1,5 (pas une puissance entière)  <br/> |
   

