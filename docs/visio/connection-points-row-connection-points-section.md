---
title: Connection Points, ligne (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3005
localization_priority: Normal
ms.assetid: eaac62a5-f516-9b81-587a-8e0e02de59ee
description: Contient les coordonnées x - et y-coordonnées, direction horizontale et verticale et type pour une seule connexion point sur une forme. Coordonnées des points de connexion sont mesurées à partir de l’origine de la forme. Une forme contient une ligne Connection Points pour chaque point de connexion.
ms.openlocfilehash: f1b8daf7f9845b85e76020c7f89c8c42b4500823
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788339"
---
# <a name="connection-points-row-connection-points-section"></a>Connection Points, ligne (section Connection Points)

Contient les coordonnées *x* - et *y* -coordonnées, direction horizontale et verticale et type pour une seule connexion point sur une forme. Coordonnées des points de connexion sont mesurées à partir de l’origine de la forme. Une forme contient une ligne Connection Points pour chaque point de connexion. 
  
Si les lignes Connection Points sont nommées, leurs noms apparaissent en tant que connexions. *nom* dans la fenêtre feuille ShapeSheet. Les lignes Connection Points contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |*X* -coordonnées d’un point de connexion dans le système de coordonnées local.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |La valeur *y* -coordonnées d’un point de connexion dans le système de coordonnées local.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |*X* -composant requis vecteur d’alignement d’un point de connexion correspondant. Il est également utilisé pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |La valeur *y* -composant requis vecteur d’alignement d’un point de connexion correspondant. Il est également utilisé pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point.  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |Type du point de connexion (0 = vers l'intérieur; 1 = vers l'extérieur; 2 = vers l'intérieur et l'extérieur).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Cellule de montage utilisable pour entrer ou tester des formules. Pour accéder à cette cellule, une ligne d’avec le bouton droit, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel.  <br/> |
   
## <a name="remarks"></a>Remarques

Cellules dans les connexions. *nom* sont intitulées DirX/A, DirY/B et Type/C car ces lignes peuvent être des lignes étendues ou non étendues. 
  
La plupart des points de connexion (tous les points de connexion créées par le biais de l’interface utilisateur) sont non étendues et ont DirX, DirY et Type de cellules. Le type de ligne est **visTagCnnctPt** ou **visTagCnnctNamed.**
  
Dans les lignes non étendues, les cellules DirX et DirY définissent ensemble un vecteur de direction qui influence la rotation des formes impliquées dans les connexions utilisant le point de connexion. Si les deux cellules ont la valeur zéro, le point n'a pas de direction. Les points de connexion sont des types suivants :
  
- Vers l'intérieur (0), ce qui signifie que les formes collent aux points de connexion. Il s'agit de la valeur par défaut.
    
- Vers l'extérieur (1), ce qui signifie que ces points de connexion vont coller aux points de connexion vers l'intérieur.
    
- Vers l'intérieur et l'extérieur (2), auquel cas la direction se fait vers l'intérieur, et est inversée si elle est utilisée comme une connexion vers l'extérieur.
    
Les lignes étendues que les cellules A, B, C et D et se comportent comme des lignes non étendues direction de type vers l’intérieur. Les lignes étendues ne sont pas couramment utilisés, mais vous pouvez les utiliser pour associer des données à un point de connexion dans les cellules A, B, C et D. Le type de ligne est **visTagCnnctPtABCD** ou **visTagCnnctNamedABCD**. Les lignes étendues peuvent être identifiés par la présence d’une formule dans la cellule D. 
  
 Vous pouvez ajouter autant de connexions.  *nom de* lignes que vous le souhaitez, assigner des noms explicites aux lignes et définir des valeurs de cellule. Pour ajouter un point de connexion à une section Connection Points existante, cliquez sur une ligne, cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez référencer des cellules de ligne de Points de connexion par leur nom de ligne, qui s’affiche dans une fenêtre feuille ShapeSheet en texte rouge. Pour modifier le nom de ligne, cliquez dessus, puis tapez un nom tel que *personnalisé* , par exemple, pour créer le nom de ligne Connections.personnalisée. Vous pouvez ensuite référencer la cellule X à l’aide d’instruction Connections.personnalisée.x, par exemple, ou Connections.X1 si vous souhaitez utiliser le numéro de ligne. 
  
Le nom de ligne que vous entrez doit être unique dans la section. Lorsque vous créez un nom pour une ligne dans la section Connection Points, Microsoft Office Visio nomme toutes les lignes dans la section avec le nom par défaut, Connections.Row_ *n* . 
  
Les lignes Connection Points nommées ne sont pas compatibles avec les versions de Visio antérieures à Visio 5.0. Lorsque vous enregistrez un fichier de dessin Visio 5.0 avec des lignes Connection Points nommées dans le format d'une version antérieure, les références aux lignes Connection Points nommées sont converties en références indexées, et les noms de lignes sont perdus.
  

