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
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423866"
---
# <a name="about-error-values"></a>À propos des valeurs d’erreur

Des valeurs d'erreur s'affichent dans les cellules contenant une formule incorrecte.
  
Si une formule fait référence à une cellule qui contient une valeur d'erreur, elle affiche également une valeur d'erreur. Utilisez les fonctions ISERR, ISERRNA, ISERROR ou ISERRVALUE pour déterminer le sens de ces valeurs d'erreur.
  
**Valeurs d'erreur**

||||
|:-----|:-----|:-----|
|**Si la cellule affiche** <br/> |**La formule contient** <br/> |**Exemple** <br/> |
| #DIV/0!  <br/> |Une division par 0  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Un argument ou un opérande de type incorrect  <br/> | 5 + "Maison"  <br/> |
| #REF!  <br/> | Une référence à une cellule qui n'existe pas  <br/> | Une cellule faisant référence à une cellule qui n'existe plus  <br/> |
| #NUM!  <br/> | Un nombre incorrect  <br/> | La racine carrée d'un nombre négatif  <br/> |
| #N/A!  <br/> | Valeur non disponible  <br/> | Fonction NA( )  <br/> |
| #DIM !  <br/> | Valeur dimensionnelle qui dépasse la plage de dimensions (les puissances valides sont des nombres -128 \< = n \< = 127)  <br/> Une valeur de cote utilisée dans une opération non appropriée  <br/> |1in^100 1in^100 (le résultat est 1in^200, ce qui se trouve au-delà de la \* plage de dimensions)  <br/> 5,2 cm^1,5 (la puissance n'est pas un entier)  <br/> |
   

