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
description: Contient les coordonnées x et y, le sens horizontal et vertical et le type d'un point de connexion unique sur une forme. Les coordonnées des points de connexion sont mesurées à partir de l'origine de la forme. Une forme contient une ligne Connection Points pour chaque point de connexion.
ms.openlocfilehash: 301ea4fb446d9acafd4b59af388c3e7b2d419e20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415508"
---
# <a name="connection-points-row-connection-points-section"></a>Connection Points, ligne (section Connection Points)

Contient les coordonnées *x* et *y* , le sens horizontal et vertical et le type d'un point de connexion unique sur une forme. Les coordonnées des points de connexion sont mesurées à partir de l'origine de la forme. Une forme contient une ligne Connection Points pour chaque point de connexion. 
  
Si les lignes Connection Points sont nommées, leurs noms apparaissent sous la forme Connections. *nom* dans la fenêtre ShapeSheet. Les lignes Connection Points contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules. 
  
|**Cellule**|**Description**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |Coordonnée *x* d'un point de connexion en coordonnées locales.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |Coordonnée *y* d'un point de connexion en coordonnées locales.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |Composant *x* pour le vecteur d'alignement requis d'un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Elle accepte une valeur à virgule flottante.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |Composant *y* pour le vecteur d'alignement requis d'un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Elle accepte une valeur à virgule flottante.  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |Type du point de connexion (0 = vers l'intérieur; 1 = vers l'extérieur; 2 = vers l'intérieur et l'extérieur).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Cellule de montage utilisable pour entrer ou tester des formules. Pour accéder à cette cellule, cliquez avec le bouton droit de la souris sur une ligne, puis choisissez **Modifier le type de ligne** dans le menu contextuel.<br/> |
   
## <a name="remarks"></a>Remarques

Les cellules de la ligne Connections. *nom* les lignes sont intitulées DirX/A, DirY/B et type/C, car ces lignes peuvent être étendues ou non étendues. 
  
La plupart des points de connexion (tous les points de connexion créés via l'interface utilisateur) ne sont pas étendus et possèdent des cellules DirX, DirY et Type. Leur type de ligne est **visTagCnnctPt** ou **visTagCnnctNamed.**
  
Dans les lignes non étendues, les cellules DirX et DirY définissent ensemble un vecteur de direction qui influence la rotation des formes impliquées dans les connexions utilisant le point de connexion. Si les deux cellules ont la valeur zéro, le point n'a pas de direction. Les points de connexion sont des types suivants :
  
- Vers l'intérieur (0), ce qui signifie que les formes collent aux points de connexion. Il s'agit de la valeur par défaut.
    
- Vers l'extérieur (1), ce qui signifie que ces points de connexion vont coller aux points de connexion vers l'intérieur.
    
- Vers l'intérieur et l'extérieur (2), auquel cas la direction se fait vers l'intérieur, et est inversée si elle est utilisée comme une connexion vers l'extérieur.
    
Les lignes étendues possèdent des cellules A, B, C et D et se comportent comme des lignes non étendues sans direction de type Vers l'intérieur. Les lignes étendues ne sont pas fréquemment utilisées mais vous pouvez les employer pour associer des données à un point de connexion dans les cellules A, B, C et D. Leur type de ligne est **visTagCnnctPtABCD** ou **visTagCnnctNamedABCD**. Les lignes étendues peuvent être identifiées par la présence d'une formule dans la cellule D. 
  
 Vous pouvez ajouter autant de lignes Connections.  *Nommez* les lignes selon vos besoins, assignez des noms parlants aux lignes et définissez des valeurs de cellule. Pour ajouter un point de connexion à une section Connection Points existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner les cellules d'une ligne Connection Points à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour modifier le nom de la ligne, cliquez sur celle-ci, puis tapez un nom tel que *personnalisé* , par exemple, pour créer le nom de ligne Connections. Custom. Vous pouvez ensuite faire référence à la cellule X à l'aide de l'instruction Connections.Personnalisée.X par exemple, ou Connections.X1 si vous souhaitez utiliser le numéro de ligne. 
  
Le nom de ligne que vous entrez doit être unique dans la section. Lorsque vous créez un nom pour une ligne dans la section Connection points, Microsoft Office Visio nomme toutes les lignes de la section avec le nom par défaut Connections. Row_ *n* . 
  
Les lignes Connection Points nommées ne sont pas compatibles avec les versions de Visio antérieures à Visio 5.0. Lorsque vous enregistrez un fichier de dessin Visio 5.0 avec des lignes Connection Points nommées dans le format d'une version antérieure, les références aux lignes Connection Points nommées sont converties en références indexées, et les noms de lignes sont perdus.
  

