---
title: Élément de la section (Sheet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Spécifie une collection de propriétés connexes.
ms.openlocfilehash: 7cb5e1c30960e69b252abc7af38e021607fd3502
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789611"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Élément de la section (Sheet_Type, complexType) (« Visio XML »)

Spécifie une collection de propriétés connexes.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.XML, masters.xml, maître # .xml, pages.xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’un dessin.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’une page dans un dessin.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Type complexe Master_Type](master_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés de la page de dessin associé à la forme de base.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés associées à une forme.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés associées à un style, dessin, dessin page ou shape.  <br/> |
|[Feuille de style](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Spécifie une feuille de style.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
|[Row](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Spécifie une collection d’éléments **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPPR.  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si une collection devant être héritée a été supprimée. Il doit être égale à 0 ou 1. Une valeur de 1 indique que la collection n’est pas utilisée et doit être ignorée. Une valeur de 0 indique que la collection de propriétés est valide pour la forme. Si l’attribut **Del** n’est pas présent, la valeur est 0.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’index de base zéro de l’élément. Il doit être unique parmi tous les éléments **Section_Type** avec le même attribut **N** du conteneur **Sheet_Type**. Il doit être supérieure à l’attribut **IX** de n’importe quel élément **Section_Type** précédente avec le même attribut **N** du conteneur **Sheet_Type**.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> |Spécifie le nom indépendant du langage de la collection de propriétés. Il doit être unique parmi tous les éléments **Section_Type** de l’élément **Sheet_Type** contenant, sauf s’il est égal à « La géométrie ». Il doit être égale à un sous-titre dans les **Sections**.  <br/> |Valeurs du type xsd : String.  <br/> |
   
### <a name="remarks"></a>Remarques

L’attribut **N** de cet élément de la **Section** doit être un ensemble limité de valeurs qui correspondent à des cellules **ShapeSheet** . Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de la **Section** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Actions  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule. Il doit avoir un élément parent **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Actions, section](actions-section.md) <br/> |
|ActionTag  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule uniquement. Il doit avoir un élément parent **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Section de balise d'action](action-tag-section.md) <br/> |
|Connexions  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule uniquement. Il doit avoir un élément parent de **ShapeSheet_Type** .  <br/> ||
|Contrôles  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule uniquement. Il doit avoir un élément parent de **ShapeSheet_Type** .  <br/> |[Controls, section](controls-section.md) <br/> |
|Lien hypertexte  <br/> |Une collection de propriétés associées qui spécifient les liens hypertexte de la forme. Il doit avoir un élément parent de **ShapeSheet_Type** .  <br/> |[Hyperlinks, section](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Une collection de propriétés associées qui spécifient les données de forme. Il doit avoir un élément parent de **ShapeSheet_Type** .  <br/> |[Shape Data, section](shape-data-section.md) <br/> |
|Utilisateur  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule. Il doit avoir un élément parent **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[User-defined Cells, section](user-defined-cells-section.md) <br/> |
   
L’attribut **IX** de cet élément de la **Section** doit être un ensemble limité de valeurs qui correspondent à des cellules **ShapeSheet** . Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **IX** qui sont autorisées pour cet élément de la **Section** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Annotation  <br/> |Une collection de propriétés qui contiennent des informations sur les commentaires insérés sur une page de document.  <br/> |[Annotation, section](annotation-section.md) <br/> |
|Caractère  <br/> |Une collection de propriétés associées qui spécifient les propriétés de caractères du texte d’une forme. Il doit avoir un élément parent de **ShapeSheet_Type** ou d’un élément parent de **StyleSheet_Type** .  <br/> |[Character, section](character-section.md) <br/> |
|Connexions  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule uniquement. Il doit avoir un élément parent de **ShapeSheet_Type** .  <br/> |[Connection Points, section](connection-points-section.md) <br/> |
|Champ  <br/> |Une collection de propriétés associées qui spécifient les champs de texte d’une forme. Il doit avoir un élément parent de **ShapeSheet_Type** .  <br/> |[Text Fields, section](text-fields-section.md) <br/> |
|FillGradient  <br/> |Une collection de propriétés qui spécifient le dégradé de couleur de remplissage d’une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Section dégradée de remplissage](fill-gradient-section.md) <br/> |
|Geometry  <br/> |Une collection de propriétés associées qui spécifient la visualisation de géométrie. Il doit avoir un élément parent de **ShapeSheet_Type** . Le premier élément enfant de **Row_Type** de cet élément doit être de type MoveTo, RelMoveTo, Ellipse ou InfiniteLine.  <br/> |[Geometry, section](geometry-section.md) <br/> |
|Layers  <br/> |Une collection de propriétés qui affiche tous les calques définis sur une page de dessin. Il doit être l’enfant d’un élément **PageSheet_Type** .  <br/> |[Layers, section](layers-section.md) <br/> |
|Dégradé de ligne  <br/> |Une collection de propriétés associées qui spécifient le dégradé de couleur de trait d’une forme. Il doit avoir un élément parent **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Section dégradé de ligne](line-gradient-section.md) <br/> |
|Paragraph  <br/> |Une collection de propriétés associées qui spécifient les propriétés de paragraphe du texte d’une forme. Il doit avoir un élément parent de **ShapeSheet_Type** ou d’un élément parent de **StyleSheet_Type** .  <br/> |[Paragraph, section](paragraph-section.md) <br/> |
|Reviewer  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule. Il doit avoir un élément parent de **DocumentSheet_Type** .  <br/> |[Reviewer, section](reviewer-section.md) <br/> |
|Montage  <br/> |Une collection de propriétés qui sont utilisés pour l’évaluation de formule. Il doit avoir un élément parent **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[Scratch, section](scratch-section.md) <br/> |
|Onglets  <br/> |Une collection de propriétés associées qui spécifient les propriétés des onglets du texte d’une forme. Il doit avoir un élément parent de **ShapeSheet_Type** ou d’un élément parent de **StyleSheet_Type** .  <br/> |[Tabs, section](tabs-section.md) <br/> |
   

