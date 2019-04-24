---
title: Élément de cellule (ligne de connexion) («Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contient les coordonnées x ou y, le sens horizontal ou vertical, ou le type d'un point de connexion unique sur une forme.
ms.openlocfilehash: 367d7e462c1eb5b8fa6ee0572346f45ad621fa15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356104"
---
# <a name="cell-element-connection-row-visio-xml"></a>Élément de cellule (ligne de connexion) («Visio XML»)

Contient les coordonnées x ou y, le sens horizontal ou vertical, ou le type d'un point de connexion unique sur une forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Master #. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de ligne (section connexion)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x et y, la direction horizontale et verticale et le type d'un point de connexion simple sur une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, le sens horizontal et vertical et le type d'un point de connexion unique sur une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur **E** est la valeur actuelle (chaîne de message d'erreur); la valeur de l'attribut **V** est la dernière valeur valide.  <br/> |Chaîne de message d'erreur.  <br/> |
|F  <br/> |xsd: String  <br/> |facultatif  <br/> | Représente la formule de l'élément. Cet attribut peut contenir l'une des chaînes suivantes:  <br/>  ' (une formule) 'si la formule existe localement  <br/>  `No Formula`Si la formule est supprimée ou bloquée localement  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Consultez la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente une unité de mesure la valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L'attribut **N** de cet élément de **cellule** doit correspondre à l'un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet. RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Value**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|AutoGen  <br/> |Indique si le point de connexion est généré automatiquement. La valeur 1 indique que le point de connexion est généré automatiquement.  <br/> |Aucun.  <br/> |
|Cellule  <br/> |Détermine le composant x du vecteur d'alignement requis d'un point de connexion correspondant.  <br/> |[DirX / A, cellule (section Connection Points)](dirxa-cell-connection-points-section.md) <br/> |
|Cellule DirY  <br/> |Détermine le composant y du vecteur d'alignement requis d'un point de connexion correspondant.  <br/> |[DirY / B, cellule (section Connection Points)](diryb-cell-connection-points-section.md) <br/> |
|Invite  <br/> |Cet attribut est réservé à un usage ultérieur.  <br/> |Aucun.  <br/> |
|Type  <br/> |Définit le type du point de connexion.  <br/> |[Type / C, cellule (section Connection Points)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Représente la coordonnée x d'un point de connexion, exprimée dans le système de coordonnées locales.  <br/> |[X, cellule (section Connection Points)](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Détermine la coordonnée y d'un point de connexion en coordonnées locales.  <br/> |[Y, cellule (section Connection Points)](y-cell-connection-points-section.md) <br/> |
   

