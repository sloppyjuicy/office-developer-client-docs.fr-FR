---
title: À propos de la feuille de calcul ShapeSheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251822
localization_priority: Normal
ms.assetid: f403890d-4a3a-bacc-53d7-1b9920b23639
description: Chaque élément de Microsoft Visio (chaque document, page, style, forme, groupe, forme ou objet appartenant à un groupe, forme de base, objet provenant d’un autre programme, repère et point de repère) a une feuille de calcul ShapeSheet où sont stockées les informations qui le concernent. Cette feuille de calcul contient des informations telles que la hauteur, l’épaisseur, l’angle, la couleur et d’autres attributs qui déterminent l’aspect et le comportement de la forme.
ms.openlocfilehash: 37b2ae10b1f511197af5ccf739de91edb74e7819
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345160"
---
# <a name="about-the-shapesheet-spreadsheet"></a>À propos de la feuille de calcul ShapeSheet

Chaque élément de Microsoft Visio (chaque document, page, style, forme, groupe, forme ou objet appartenant à un groupe, forme de base, objet provenant d’un autre programme, repère et point de repère) a une feuille de calcul ShapeSheet où sont stockées les informations qui le concernent. Cette feuille de calcul contient des informations telles que la hauteur, l’épaisseur, l’angle, la couleur et d’autres attributs qui déterminent l’aspect et le comportement de la forme.
  
En tant que développeur, vous devez contrôler avec précision l’aspect et le comportement des formes que vous créez. Vous pouvez modifier le comportement par défaut d’une forme et améliorer ses capacités en la modifiant dans sa feuille ShapeSheet, à laquelle vous accédez par une fenêtre ShapeSheet ou par programme.
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a>Affichage d’un objet dans une fenêtre ShapeSheet

La fenêtre de dessin Visio et la fenêtre ShapeSheet sont simplement des vues différentes de la même forme.
  
- Lorsque vous affichez une forme dans une fenêtre de dessin, vous voyez son aspect graphique et son comportement tels qu’ils sont définis par les formules de la feuille ShapeSheet.
    
- Lorsque vous affichez une forme dans une fenêtre Feuille ShapeSheet, vous voyez les formules sous-jacentes qui déterminent son aspect et son comportement sur la page de dessin.
    
Vous pouvez afficher simultanément une fenêtre ShapeSheet et une fenêtre de dessin, et voir la forme changer dans cette dernière à mesure que vous modifiez les cellules de sa fenêtre ShapeSheet ou inversement. Si, par exemple, vous déplacez la forme avec le curseur, les formules PinX et PinY de la forme sont modifiées dans la section Shape Transform pour refléter sa nouvelle position sur la page de dessin.
  
## <a name="structure-of-the-shapesheet-window"></a>Structure de la fenêtre ShapeSheet

Une feuille ShapeSheet est divisée en *sections* qui contrôlent un aspect particulier du comportement ou de l'apparence d'une forme, par exemple sa géométrie ou sa mise en forme. Chaque section contient une ou plusieurs *lignes* qui contiennent des *cellules* . Chaque cellule peut comprendre une formule, son résultat (appelé communément « valeur » de la cellule) et des informations d’erreur facultatives. Selon la cellule, une formule peut être requise ou facultative. Les données d’une cellule (sa formule ou sa valeur, par exemple) peuvent être définies localement ou, plus souvent, héritées de la cellule équivalente de la forme de base ou du style correspondant. 
  
L'exemple suivant montre la barre de formule ![barre de formule](media/callout1_ZA01036259.gif), une section ![section](media/callout2_ZA01036260.gif), une cellule ![Cell](media/callout3_ZA01036261.gif)et une ligne ![row](media/callout4_ZA01036262.gif) dans la fenêtre ShapeSheet. 
  
![Fenêtre ShapeSheet](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
Lorsque vous dessinez une forme, Visio l’enregistre comme un ensemble d’emplacements horizontaux et verticaux reliés par des segments de trait. Ces emplacements (appelés sommets) sont enregistrés dans les cellules X et Y de la section **géométrie** de la forme. Comme le montre l'exemple suivant, lorsque vous cliquez sur les cellules X et Y dans **** la section Geometry de la fenêtre ShapeSheet d'une forme, vous verrez un cadre noir mettant en surbrillance le sommet sur la forme dans la fenêtre de dessin. 
  
![Rectangle à bordure noire mettant en surbrillance le sommet sur la forme dans la fenêtre de dessin](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a>Modification d’un objet dans la fenêtre ShapeSheet

Lorsqu’une fenêtre ShapeSheet est active, le Ruban se transforme pour afficher les options spécifiques permettant de travailler dans cette fenêtre. Lorsque vous sélectionnez une cellule ShapeSheet, une barre de formule apparaît pour vous permettre d’entrer et de modifier les formules d’un objet. Vous pouvez toutefois également travailler directement dans la cellule.
  
Dans une fenêtre ShapeSheet, vous pouvez ajouter des sections à la feuille de calcul d’une forme pour ajouter de nouvelles caractéristiques à la forme sur la page de dessin. Par exemple, vous pouvez ajouter une section **Connection points** pour créer une connexion. Lorsqu’une section n’est plus utile, vous pouvez la supprimer. 
  
Vous pouvez également ajouter des lignes aux sections afin de recevoir des formules supplémentaires ou pour modifier l’aspect d’une forme. Par exemple, vous pouvez ajouter une ligne à une **** section Geometry pour ajouter un segment à une forme. De même, vous pouvez supprimer les lignes dont vous n’avez plus besoin. 
  
Vous pouvez afficher des formules ou des valeurs dans les cellules. Affichez les formules lorsque vous en entrez une nouvelle, modifiez une formule existante ou souhaitez voir les relations existantes entre les formules de plusieurs cellules. Une valeur est le résultat de l’évaluation de la formule d’une cellule par Visio. Vous pouvez afficher les valeurs dans les cellules pour voir le résultat d’une évaluation.
  
## <a name="additional-shapesheet-references"></a>Autres références relatives à la feuille ShapeSheet

Pour plus d'informations sur une section, une ligne ou une cellule particulière dans la feuille ShapeSheet, consultez l'article correspondant dans cette [référence ShapeSheet](reference-visio-shapesheet.md).
  
Pour plus de détails sur l’accès à la feuille ShapeSheet par programme, reportez-vous à la Référence d’Automation de Microsoft Visio.
  

