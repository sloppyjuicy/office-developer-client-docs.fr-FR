---
title: Élément Shape (Shapes_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contient des éléments qui définissent une forme dans un élément Master, Page ou Group Shape.
ms.openlocfilehash: b39201fb420c1191aa035de630a376d3de020b59
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773907"
---
# <a name="shape-element-shapes_type-complextype-visio-xml"></a>Élément Shape (Shapes_Type complexType) (Visio XML)

Contient des éléments qui définissent une forme dans un **élément Master**, **Page** ou Group Shape.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes. |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique. |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire utilisée pour fournir des informations supplémentaires sur une forme. |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire utilisée pour fournir des informations supplémentaires sur une forme. |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire utilisée pour fournir des informations supplémentaires sur une forme. |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contient un OBJET BLOB MIME (Multipurpose Internet Mail Extensions) codé de données d’image, telles que Windows métafichier, bitmap ou données OLE. |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés connexes. |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes. |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contient le texte d’une forme. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indicateur indiquant si l’élément est supprimé localement. |Valeurs du type xsd:boolean. |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||ID de la feuille de style dont cette forme hérite de la mise en forme du remplissage. |Valeurs du type xsd:unsignedInt. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:unsignedInt. |
|IsCustomName  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur. |Valeurs du type xsd:boolean. |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur. |Valeurs du type xsd:boolean. |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||ID de la feuille de style dont cette forme hérite de la mise en forme des lignes. |Valeurs du type xsd:unsignedInt. |
|Master  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément Master dont la forme hérite de ses données. |Valeurs du type xsd:unsignedInt. |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément Master dont la forme hérite de ses données. |Valeurs du type xsd:unsignedInt. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément. |Valeurs du type xsd:string. |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément. |Valeurs du type xsd:string. |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||ID de la feuille de style dont cette forme hérite de la mise en forme du texte. |Valeurs du type xsd:unsignedInt. |
|Type  <br/> |xsd:token  <br/> |facultatif  <br/> |Type d’une forme. Il peut s’avoir l’une des valeurs suivantes : Groupe, Forme, Guide ou Étranger. |Valeurs du type xsd:token. |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |GUID (identificateur global unique) affecté à la forme. |Valeurs du type xsd:string. |
   

