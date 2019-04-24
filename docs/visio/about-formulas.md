---
title: À propos des formules
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Les actions sur les formes sont commandées au moyen de formules que vous écrivez pour définir le comportement désiré. Vous pouvez modifier la formule d’une cellule pour en changer la valeur, et modifier ainsi le comportement d’une forme particulière. Par exemple, la cellule Height de la section Shape Transform contient une formule que vous pouvez modifier pour changer la hauteur de la forme.
ms.openlocfilehash: e8e1a2b77cc355e930af6f31f0b375dfba321e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344456"
---
# <a name="about-formulas"></a>À propos des formules

Les actions sur les formes sont commandées au moyen de formules que vous écrivez pour définir le comportement désiré. Vous pouvez modifier la formule d’une cellule pour en changer la valeur, et modifier ainsi le comportement d’une forme particulière. Par exemple, la cellule Height de la section Shape Transform contient une formule que vous pouvez modifier pour changer la hauteur de la forme.
  
Les formules Microsoft Visio ressemblent à de nombreux égards aux formules classiques des feuilles de calcul. Visio considère tout ce qui apparaît dans une cellule, même une valeur numérique ou une simple référence à une autre cellule, comme une formule.
  
La formule d’une cellule peut être héritée de la cellule équivalente d’une forme de base ou d’un style, ou être définie localement. Visio évalue la formule puis en convertit les résultats en la valeur appropriée dans l’unité adaptée pour la cellule. Dans une fenêtre Feuille ShapeSheet, vous pouvez afficher le contenu des cellules sous la forme de formules ou de valeurs.
  
## <a name="elements-of-a-formula"></a>Éléments d’une formule

Une formule commence toujours par un signe égal qui est inséré automatiquement. Une formule peut comprendre un ou plusieurs des éléments suivants :
  
- Nombres
    
- Coordinate
    
- Valeurs booléennes
    
- Opérateurs
    
- Fonctions
    
- Chaînes
    
- Références de cellule
    
- Unités de mesure
    
## <a name="default-formulas"></a>Formules par défaut

Lorsque vous créez une forme, Visio crée pour celle-ci des formules par défaut. Pour avoir un aperçu de ces formules par défaut, tracez une forme simple (rectangle, ellipse ou trait rectiligne) et ouvrez sa fenêtre Feuille ShapeSheet (sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), cliquez sur **Afficher la feuille ShapeSheet**).
  
## <a name="inherited-formulas"></a>Formules héritées

Visio applique l’héritage des formules chaque fois que possible. Au lieu de copier localement chaque formule de l’instance, cette instance hérite des formules de sa forme de base dans le gabarit du document et de sa mise en forme dans les définitions de style enregistrées avec le dessin. Cette méthode permet de réduire la taille des fichiers, mais aussi de propager à toutes les instances les modifications de formules de la forme de base ou de la définition de style.
  
Du texte en noir dans une cellule indique une formule héritée.
  
## <a name="local-formulas"></a>Formules locales

Lorsque vous écrivez une formule locale pour une instance, vous remplacez la formule héritée par une formule locale dans la cellule. Les modifications apportées par la suite à cette cellule dans la forme de base ou dans le style n’affectent pas cette instance étant donné que la formule locale a annulé l’héritage.
  
L’application d’un style supprime toutes les formules locales des cellules concernées sauf si vous utilisez la fonction GUARD pour les protéger.
  
Le texte en bleu indique une formule locale, résultat de la modification de la formule dans une fenêtre Feuille ShapeSheet ou de modifications de la forme ayant amené Visio à redéfinir la formule de cette cellule.
  
## <a name="automatic-updates-to-formulas"></a>Mises à jour automatiques des formules

 Visio met automatiquement à jour certaines cellules à chaque modification d’une forme dans un dessin. Ainsi, dans certaines circonstances, les formules que vous avez entrées peuvent être remplacées. Par exemple, si vous faites glisser une poignée de coin pour redimensionner une forme, Visio redéfinit les formules des cellules PinX, PinY, Width et Height. 
  
Au besoin, vous pouvez protéger les formules locales à l’aide de la fonction GUARD.
  

