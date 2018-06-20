---
title: Élément de cellule (ligne Ellipse) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 210e6731-7c94-90b1-c7c4-635df974fdb6
description: Contient les coordonnées x ou y du centre et de deux points sur l’ellipse.
ms.openlocfilehash: 40458d7d9945897fd9d8f9764ff6b81884490b1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788215"
---
# <a name="cell-element-ellipse-row-visio-xml"></a>Élément de cellule (ligne Ellipse) (« Visio XML »)

Contient les coordonnées x ou y du centre et de deux points sur l’ellipse.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master # .xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Ellipse_Type](ellipse_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du centre et de deux points sur l’ellipse.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD : String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur de **E** est la valeur actuelle (chaîne message d’erreur) ; la valeur de l’attribut de **V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |XSD : String  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir une des chaînes suivantes :  <br/>  « (une formule) » si la formule existe localement  <br/>  `No Formula`Si la formule est localement supprimée ou bloquée  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> |Représente le nom de la cellule de feuille ShapeSheet.  <br/> |Le nom de la cellule de feuille ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente une unité de mesure par défaut est la liste de distribution.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |La valeur de la cellule de feuille ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément de **cellule** doit être un ensemble limité de valeurs qui correspondent à des cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|X   <br/> |Coordonnée x du point central.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|Y  <br/> |Coordonnée y du point central.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|A  <br/> |Coordonnée x du premier point sur l’ellipse ; associée à la coordonnée y représentée par la cellule B.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|B  <br/> |Coordonnée y du premier point sur l’ellipse ; associée à la coordonnée x représentée par la cellule A.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|C  <br/> |Coordonnée x du deuxième point sur l’ellipse ; associée à la coordonnée y représentée par la cellule D.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|D  <br/> |Coordonnée y du deuxième point sur l’ellipse ; associée à la coordonnée y représentée par la cellule C.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
   

