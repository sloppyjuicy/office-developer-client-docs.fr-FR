---
title: Élément Row (Layer Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contient des éléments qui définissent une couche unique et ses propriétés pour une page.
ms.openlocfilehash: 035046a0a3ac02210d3bc47acd4a5613796fb8ac
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779402"
---
# <a name="row-element-layer-section-visio-xml"></a>Élément Row (Layer Section) (Visio XML)

Contient des éléments qui définissent une couche unique et ses propriétés pour une page.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |masters.xml, pages.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une couche unique et ses propriétés pour une page. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété pour un calque ou ses propriétés pour une page. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui sinon serait héritée d’une forme de forme de maître a été supprimée. |Valeurs du type xsd:boolean. |
|IX  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur à base un de la ligne. Il doit être unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs. Une ligne ne peut avoir qu’un des attributs IX ou N. |Valeurs du type xsd:unsignedInt. |
|LocalName  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne. |Valeurs du type xsd:string. |
|N  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag. Une ligne ne peut avoir qu’un des attributs IX ou N. |Valeurs du type xsd:string. |
|T  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisé uniquement pour la section Geometry. |Valeurs du type xsd:string. |
   

