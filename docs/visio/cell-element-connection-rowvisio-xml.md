---
title: Élément de cellule (ligne Connection) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contient les coordonnées x ou y, la direction horizontale ou verticale, ou le type d’un point de connexion unique sur une forme.
ms.openlocfilehash: 0c8177767d5c85d505ba8a2a430946fd29cf44aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541875"
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Connection Section)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x et y, la direction horizontale et verticale et le type d'un point de connexion simple sur une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la direction horizontale et verticale et le type d’un point de connexion unique sur une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée.  <br/> |Formule.  <br/> |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit faire partie d’un ensemble limité de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell.** 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|AutoGen  <br/> |Spécifie si le point de connexion est généré automatiquement. La valeur 1 indique que le point de connexion est généré automatiquement.  <br/> |Aucun.  <br/> |
|DirX  <br/> |Détermine le composant x du vecteur d'alignement requis d'un point de connexion correspondant.  <br/> |[DirX / A, cellule (section Connection Points)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Détermine le composant y du vecteur d'alignement requis d'un point de connexion correspondant.  <br/> |[DirY / B, cellule (section Connection Points)](diryb-cell-connection-points-section.md) <br/> |
|Invite  <br/> |Cet attribut est réservé à un usage ultérieur.  <br/> |Aucun.  <br/> |
|Type  <br/> |Définit le type du point de connexion.  <br/> |[Type / C, cellule (section Connection Points)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Représente la coordonnée x d'un point de connexion, exprimée dans le système de coordonnées locales.  <br/> |[X, cellule (section Connection Points)](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Détermine la coordonnée y d’un point de connexion dans les coordonnées locales.  <br/> |[Y, cellule (section Connection Points)](y-cell-connection-points-section.md) <br/> |
   

