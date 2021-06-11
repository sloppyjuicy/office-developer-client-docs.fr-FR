---
title: Élément Shape (Shapes_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contient des éléments qui définissent une forme dans un élément Master, Page ou Group Shape.
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542071"
---
# <a name="shape-element-shapes_type-complextype-visio-xml"></a>Élément Shape (Shapes_Type complexType) (Visio XML)

Contient des éléments qui définissent une forme dans un **élément de forme de** groupe, page ou maître. 
  
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Formes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
|[Formes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire utilisée pour fournir des informations supplémentaires sur une forme.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire utilisée pour fournir des informations supplémentaires sur une forme.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire utilisée pour fournir des informations supplémentaires sur une forme.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contient un OBJET BLOB MIME (Multipurpose Internet Mail Extensions) codé de données d’image, telles que Windows métafichier, bitmap ou données OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés connexes.  <br/> |
|[Formes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contient le texte d’une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indicateur indiquant si l’élément est supprimé localement.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||ID de la feuille de style dont cette forme hérite de la mise en forme du remplissage.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||ID de la feuille de style dont cette forme hérite de la mise en forme des lignes.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément Master dont la forme hérite de ses données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément Master dont la forme hérite de ses données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||ID de la feuille de style dont cette forme hérite de la mise en forme du texte.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Type  <br/> |xsd:token  <br/> |facultatif  <br/> |Type d’une forme. Il peut s’avoir l’une des valeurs suivantes : Groupe, Forme, Guide ou Étranger.  <br/> |Valeurs du type xsd:token.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |GUID (identificateur global unique) affecté à la forme.  <br/> |Valeurs du type xsd:string.  <br/> |
   

