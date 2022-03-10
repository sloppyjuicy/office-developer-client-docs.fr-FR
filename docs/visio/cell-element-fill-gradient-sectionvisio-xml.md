---
title: Élément de cellule (section Fill Gradient) (Visio XML)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: Contient la couleur, la transparence et la position d’un dégradé pour un dégradé de remplissage.
ms.openlocfilehash: a6105c9a969a7700839cfc3f9b376f120a7d6d0a
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406407"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a>Élément de cellule (section Fill Gradient) (Visio XML)

Contient la couleur, la transparence et la position d’un dégradé pour un dégradé de remplissage.
  
## <a name="element-information"></a>Informations sur l'élément

|**Valeur**|**Description**|
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (FillGradient Section)](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un dégradé pour un dégradé de remplissage. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin. |
   
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
|GradientStopColor  <br/> |Valeur de couleur du dégradé. Cette valeur peut être exprimée en tant que numéro d’index d’une couleur dans la palette de documents ou à l’aide des fonctions **RVB**, **THEMEVAL** ou **HSL** . |[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |Quantité de transparence du point de dégradé, sous la mesure d’un pourcentage. |[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |Position du point de dégradé le long de la direction du dégradé de trait, sous la mesure d’un pourcentage entre le point d’origine du dégradé et le bord externe du dégradé. |[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md) <br/> |  
