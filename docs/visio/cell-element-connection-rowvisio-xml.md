---
title: Élément de cellule (ligne Connection) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contient les coordonnées x ou y, la direction horizontale ou verticale, ou le type d’un point de connexion unique sur une forme.
ms.openlocfilehash: 0b061c3687c6a8b1f953b04e80132bfc1ea0be0e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775989"
---
# <a name="cell-element-connection-row-visio-xml"></a>Élément de cellule (ligne Connection) (Visio XML)

Contient les coordonnées x ou y, la direction horizontale ou verticale, ou le type d’un point de connexion unique sur une forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Connection Section)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x et y, la direction horizontale et verticale et le type d'un point de connexion simple sur une forme. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la direction horizontale et verticale, et le type d’un point de connexion unique sur une forme. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide. |Chaîne de message d’erreur. |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée. |Formule. |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet. |Nom de la cellule ShapeSheet. Voir la section Remarques ci-dessous. |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL. |Unités de la cellule. |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule. |Valeur de la cellule ShapeSheet. |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit être l’un des ensembles limités de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|AutoGen  <br/> |Spécifie si le point de connexion est généré automatiquement. La valeur 1 indique que le point de connexion est généré automatiquement. |Aucun. |
|DirX  <br/> |Détermine le composant x du vecteur d'alignement requis d'un point de connexion correspondant. |[DirX / A, cellule (section Connection Points)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Détermine le composant y du vecteur d'alignement requis d'un point de connexion correspondant. |[DirY / B, cellule (section Connection Points)](diryb-cell-connection-points-section.md) <br/> |
|Invite  <br/> |Cet attribut est réservé à un usage ultérieur. |Aucun. |
|Type  <br/> |Définit le type du point de connexion. |[Type / C, cellule (section Connection Points)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Représente la coordonnée x d'un point de connexion, exprimée dans le système de coordonnées locales. |[X, cellule (section Connection Points)](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Détermine la coordonnée y d’un point de connexion dans les coordonnées locales. |[Y, cellule (section Connection Points)](y-cell-connection-points-section.md) <br/> |
   

