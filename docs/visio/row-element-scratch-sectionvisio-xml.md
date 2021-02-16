---
title: Élément Row (section Scratch) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541000"
---
# <a name="row-element-scratch-section-visio-xml"></a>Élément Row (section Scratch) (Visio XML)

Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ScratchRow_Type](scratchrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui sinon serait héritée d’une forme de forme de maître a été supprimée.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur à base un de la ligne. Il doit être unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisé uniquement pour la section Geometry.  <br/> |Valeurs du type xsd:string.  <br/> |
   

