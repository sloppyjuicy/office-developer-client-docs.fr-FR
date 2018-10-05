---
title: Élément de cellule (ligne de connexion) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contient les coordonnées x ou y, sens horizontal ou vertical ou le type d’un point de connexion unique d’une forme.
ms.openlocfilehash: 367d7e462c1eb5b8fa6ee0572346f45ad621fa15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388958"
---
# <a name="cell-element-connection-row-visio-xml"></a>Élément de cellule (ligne de connexion) (« Visio XML »)

Contient les coordonnées x ou y, sens horizontal ou vertical ou le type d’un point de connexion unique d’une forme.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Élément de ligne (section Connexion)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x et y, direction horizontale et verticale et le type d’un point de connexion unique d’une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, direction horizontale et verticale et le type d’un point de connexion unique d’une forme.  <br/> |
   
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
|AutoGen  <br/> |Spécifie si le point de connexion est automatiquement généré. Une valeur de 1 indique que le point de connexion est généré automatiquement.  <br/> |Aucune.  <br/> |
|DirX  <br/> |Détermine le composant x pour le vecteur d’alignement requis d’un point de connexion correspondant.  <br/> |[DirX / A, cellule (section Connection Points)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Détermine le composant y du vecteur d’alignement requis d’un point de connexion correspondant pour.  <br/> |[DirY / B, cellule (section Connection Points)](diryb-cell-connection-points-section.md) <br/> |
|Prompt  <br/> |Cet attribut est réservé pour une utilisation future.  <br/> |Aucune.  <br/> |
|Type  <br/> |Définit le type du point de connexion.  <br/> |[Type / C, cellule (section Connection Points)](typec-cell-connection-points-section.md) <br/> |
|X   <br/> |Représente la coordonnée x d'un point de connexion, exprimée dans le système de coordonnées locales.  <br/> |[X, cellule (section Connection Points)](x-cell-connection-points-section.md) <br/> |
|Y  <br/> |Détermine la coordonnée y d’un point de connexion dans le système de coordonnées local.  <br/> |[Y, cellule (section Connection Points)](y-cell-connection-points-section.md) <br/> |
   

