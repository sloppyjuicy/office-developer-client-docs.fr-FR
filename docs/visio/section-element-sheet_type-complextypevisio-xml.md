---
title: Élément Section (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Spécifie une collection de propriétés connexes.
ms.openlocfilehash: dfddb027a552fb54b60f05371addb99da1211593
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778201"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Élément Section (Sheet_Type complexType) (Visio XML)

Spécifie une collection de propriétés connexes.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’un dessin. |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’une page dans un dessin. |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés de la page de dessin associée à la page de dessin. |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés associées à une forme. |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés associées à un style, un dessin, une page de dessin ou une forme. |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Spécifie une feuille de style. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique. |
|[Ligne](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Spécifie une collection **d’Cell_Type** éléments. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si une collection héritée a été supprimée. Elle DOIT être égale à 0 ou 1. La valeur 1 spécifie que la collection est inutilisée et DOIT être ignorée. La valeur 0 indique que la collection de propriétés est valide pour la forme. Si **l’attribut Del** n’est pas présent, la valeur est 0. |Valeurs du type xsd:boolean. |
|IX  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’index de base zéro de l’élément. Il DOIT être unique parmi tous les éléments **Section_Type** avec le même attribut **N** du **Sheet_Type.** Il DOIT être supérieur à **l’attribut IX** de tout **élément Section_Type** précédent avec le même attribut **N** du **Sheet_Type.** |Valeurs du type xsd:unsignedInt. |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le nom indépendant de la langue de la collection de propriétés. Il DOIT être unique parmi tous les éléments Section_Type  de l’élément Sheet_Type contenant,  sauf s’il est égal à « Geometry ». Il DOIT être égal à un sous-en-tête dans **Sections**. |Valeurs du type xsd:string. |
   
### <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Section** doit être l’un des ensembles limités de valeurs qui correspondent aux **cellules ShapeSheet**. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Section** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Actions  <br/> |Collection de propriétés utilisées pour l’évaluation de formule. Elle DOIT avoir un **élément ShapeSheet_Type** ou **PageSheet_Type** parent. |[Actions, section](actions-section.md) <br/> |
|ActionTag  <br/> |Collection de propriétés utilisées uniquement pour l’évaluation de formule. Elle DOIT avoir un **élément ShapeSheet_Type** ou **PageSheet_Type** parent. |[Section de balise d'action](action-tag-section.md) <br/> |
|Connexions  <br/> |Collection de propriétés utilisées uniquement pour l’évaluation de formule. Elle DOIT avoir un **élément ShapeSheet_Type** parent. ||
|Contrôles  <br/> |Collection de propriétés utilisées uniquement pour l’évaluation de formule. Elle DOIT avoir un **élément ShapeSheet_Type** parent. |[Controls, section](controls-section.md) <br/> |
|Hyperlink  <br/> |Collection de propriétés associées qui spécifient les liens hypertexte de forme. Elle DOIT avoir un **élément ShapeSheet_Type** parent. |[Hyperlinks, section](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Collection de propriétés associées qui spécifient les données de forme. Elle DOIT avoir un **élément ShapeSheet_Type** parent. |[Shape Data, section](shape-data-section.md) <br/> |
|Utilisateur  <br/> |Collection de propriétés utilisées pour l’évaluation de formule. Elle DOIT avoir un **élément DocumentSheet_Type**, **PageSheet_Type** ou **ShapeSheet_Type** parent. |[User-defined Cells, section](user-defined-cells-section.md) <br/> |
   
**L’attribut IX** de cet **élément Section** doit faire partie d’un ensemble limité de valeurs qui correspondent aux **cellules ShapeSheet**. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de **l’attribut IX** qui sont autorisées pour cet **élément Section** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Annotation  <br/> |Collection de propriétés qui contiennent des informations sur les commentaires insérés dans une page de document. |[Annotation, section](annotation-section.md) <br/> |
|Caractère  <br/> |Collection de propriétés associées qui spécifient les propriétés de caractère du texte d’une forme. Elle DOIT avoir un **ShapeSheet_Type** parent ou un **StyleSheet_Type** parent. |[Character, section](character-section.md) <br/> |
|Connexions  <br/> |Collection de propriétés utilisées uniquement pour l’évaluation de formule. Elle DOIT avoir un **élément ShapeSheet_Type** parent. |[Connection Points, section](connection-points-section.md) <br/> |
|Champ  <br/> |Collection de propriétés associées qui spécifient les champs de texte d’une forme. Elle DOIT avoir un **élément ShapeSheet_Type** parent. |[Text Fields, section](text-fields-section.md) <br/> |
|FillGradient  <br/> |Collection de propriétés qui spécifient le dégradé de couleur de remplissage d’une forme. Elle DOIT avoir un **élément ShapeSheet_Type** ou **StyleSheet_Type** parent. |[Fill Gradient Section](fill-gradient-section.md) <br/> |
|Geometry  <br/> |Collection de propriétés associées qui spécifient la visualisation de la géométrie. Elle DOIT avoir un **élément ShapeSheet_Type** parent. Le premier **Row_Type** enfant de cet élément DOIT être de type MoveTo, RelMoveTo, Ellipse ou InfiniteLine. |[Geometry, section](geometry-section.md) <br/> |
|Calques  <br/> |Collection de propriétés qui affiche toutes les couches définies sur une page de dessin. Il DOIT être l’enfant **d’un PageSheet_Type** de projet. |[Layers, section](layers-section.md) <br/> |
|Dégradé de trait  <br/> |Collection de propriétés associées qui spécifient le dégradé de couleur de trait d’une forme. Elle DOIT avoir un **élément ShapeSheet_Type** ou **StyleSheet_Type** parent. |[Line Gradient Section](line-gradient-section.md) <br/> |
|Paragraphe  <br/> |Collection de propriétés associées qui spécifient les propriétés de paragraphe du texte d’une forme. Elle DOIT avoir un **ShapeSheet_Type** parent ou un **StyleSheet_Type** parent. |[Paragraph, section](paragraph-section.md) <br/> |
|Relecteur  <br/> |Collection de propriétés utilisées pour l’évaluation de formule. Elle DOIT avoir un **élément DocumentSheet_Type** parent. |[Reviewer, section](reviewer-section.md) <br/> |
|Scratch  <br/> |Collection de propriétés utilisées pour l’évaluation de formule. Elle DOIT avoir un **élément DocumentSheet_Type**, **PageSheet_Type** ou **ShapeSheet_Type** parent. |[Scratch, section](scratch-section.md) <br/> |
|Onglets  <br/> |Collection de propriétés associées qui spécifient les propriétés tabulations du texte d’une forme. Elle DOIT avoir un **ShapeSheet_Type** parent ou un **StyleSheet_Type** parent. |[Tabs, section](tabs-section.md) <br/> |
   

