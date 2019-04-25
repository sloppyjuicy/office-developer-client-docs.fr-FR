---
title: Élément section (Sheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Spécifie une collection de propriétés connexes.
ms.openlocfilehash: e20d076d4e1958cce29554d728b64385c2f8adef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "32326081"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Élément section (Sheet_Type complexType) ('Visio XML')

Spécifie une collection de propriétés connexes.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. xml, Masters. xml, Master #. xml, pages. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d'un dessin.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie les propriétés d'une page dans un dessin.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie les propriétés de la page de dessin associée à la forme de base.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés associée à une forme.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés associée à un style, un dessin, une page de dessin ou une forme.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Spécifie une feuille de style.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
|[Ligne](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Spécifie une collection d'éléments **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Suppr  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si une collection qui serait normalement héritée a été supprimée. Il doit être égal à 0 ou 1. La valeur 1 indique que la collection n'est pas utilisée et doit être ignorée. La valeur 0 indique que la collection de propriétés est valide pour la forme. Si l'attribut **del** n'est pas présent, la valeur est 0.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l'index de base zéro de l'élément. Il doit être unique parmi tous les éléments **Section_Type** avec le même attribut **N** que le conteneur **Sheet_Type**. Il doit être supérieur à l'attribut **IX** de tout élément **Section_Type** précédent avec le même attribut **N** de la **Sheet_Type**conteneur.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Spécifie le nom indépendant de la langue de la collection de propriétés. Il doit être unique parmi tous les éléments **Section_Type** de l'élément **Sheet_Type** conteneur, sauf s'il est égal à «Geometry». Il doit être égal à un sous-titre dans les **sections**.  <br/> |Valeurs du type xsd: String.  <br/> |
   
### <a name="remarks"></a>Remarques

L'attribut **N** de cet élément **section** doit correspondre à l'un des jeux de valeurs qui correspondent aux cellules de la **feuille ShapeSheet** . RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **N** qui sont autorisées pour cet élément de **section** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Actions  <br/> |Collection de propriétés qui sont utilisées pour l'évaluation d'une formule. Il doit avoir un élément parent **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Actions, section](actions-section.md) <br/> |
|ActionTag  <br/> |Collection de propriétés qui sont utilisées uniquement pour l'évaluation de formule. Il doit avoir un élément parent **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Section de balise d'action](action-tag-section.md) <br/> |
|Connections  <br/> |Collection de propriétés qui sont utilisées uniquement pour l'évaluation de formule. Il doit avoir un élément parent **ShapeSheet_Type** .  <br/> ||
|Contrôles  <br/> |Collection de propriétés qui sont utilisées uniquement pour l'évaluation de formule. Il doit avoir un élément parent **ShapeSheet_Type** .  <br/> |[Controls, section](controls-section.md) <br/> |
|Lien hypertexte  <br/> |Collection de propriétés connexes qui spécifient les liens hypertexte de la forme. Il doit avoir un élément parent **ShapeSheet_Type** .  <br/> |[Hyperlinks, section](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Collection de propriétés connexes qui spécifient les données de forme. Il doit avoir un élément parent **ShapeSheet_Type** .  <br/> |[Shape Data, section](shape-data-section.md) <br/> |
|Utilisateur  <br/> |Collection de propriétés qui sont utilisées pour l'évaluation d'une formule. Il doit avoir un élément parent **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[User-defined Cells, section](user-defined-cells-section.md) <br/> |
   
L'attribut **IX** de cet élément **section** doit correspondre à l'un des jeux de valeurs limités qui correspondent aux cellules de la **feuille ShapeSheet** . RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **IX** qui sont autorisées pour cet élément de **section** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Commentaire  <br/> |Collection de propriétés qui contiennent des informations sur les commentaires insérés dans une page de document.  <br/> |[Annotation, section](annotation-section.md) <br/> |
|Caractère  <br/> |Collection de propriétés connexes qui spécifient les propriétés de caractère du texte d'une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou un élément parent **StyleSheet_Type** .  <br/> |[Character, section](character-section.md) <br/> |
|Connections  <br/> |Collection de propriétés qui sont utilisées uniquement pour l'évaluation de formule. Il doit avoir un élément parent **ShapeSheet_Type** .  <br/> |[Connection Points, section](connection-points-section.md) <br/> |
|Field  <br/> |Collection de propriétés connexes qui spécifient les champs de texte d'une forme. Il doit avoir un élément parent **ShapeSheet_Type** .  <br/> |[Text Fields, section](text-fields-section.md) <br/> |
|FillGradient  <br/> |Collection de propriétés qui spécifient le dégradé de couleur de remplissage d'une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Fill Gradient Section](fill-gradient-section.md) <br/> |
|Géométrie  <br/> |Collection de propriétés connexes qui spécifient la visualisation de géométrie. Il doit avoir un élément parent **ShapeSheet_Type** . Le premier élément enfant **Row_Type** de cet élément doit être de type MoveTo, RelMoveTo, ellipse ou InfiniteLine.  <br/> |[Geometry, section](geometry-section.md) <br/> |
|Calques  <br/> |Collection de propriétés qui affiche tous les calques définis sur une page de dessin. Il doit s'agir de l'enfant d'un élément **PageSheet_Type** .  <br/> |[Layers, section](layers-section.md) <br/> |
|Dégradé de ligne  <br/> |Collection de propriétés connexes spécifiant le dégradé de couleur d'une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Line Gradient Section](line-gradient-section.md) <br/> |
|Paragraphe  <br/> |Collection de propriétés connexes qui spécifient les propriétés de paragraphe du texte d'une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou un élément parent **StyleSheet_Type** .  <br/> |[Paragraph, section](paragraph-section.md) <br/> |
|Relecteur  <br/> |Collection de propriétés qui sont utilisées pour l'évaluation d'une formule. Il doit avoir un élément parent **DocumentSheet_Type** .  <br/> |[Reviewer, section](reviewer-section.md) <br/> |
|Nouveau  <br/> |Collection de propriétés qui sont utilisées pour l'évaluation d'une formule. Il doit avoir un élément parent **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[Scratch, section](scratch-section.md) <br/> |
|Onglets  <br/> |Collection de propriétés connexes qui spécifient les propriétés tabs du texte d'une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou un élément parent **StyleSheet_Type** .  <br/> |[Tabs, section](tabs-section.md) <br/> |
   

