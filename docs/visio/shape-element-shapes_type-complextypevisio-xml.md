---
title: Élément Shape (Shapes_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contient des éléments qui définissent une forme dans un élément de forme de forme de base, de page ou de groupe.
ms.openlocfilehash: 6308b8dd21c92f6ced9ea7f03ec8aa85773fa2bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326571"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Élément Shape (Shapes_Type complexType) ('Visio XML')

Contient des éléments qui définissent une forme dans un élément de forme de forme de **base**, de **page**ou de groupe.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |page #. xml, Master #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Type_de_données](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire qui est utilisée pour fournir des informations supplémentaires sur une forme.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Type_de_données](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire qui est utilisée pour fournir des informations supplémentaires sur une forme.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Type_de_données](data_type-complextypevisio-xml.md) <br/> |Contient une valeur de chaîne arbitraire qui est utilisée pour fournir des informations supplémentaires sur une forme.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contient un BLOB encodé MIME (Multipurpose Internet Mail Extensions) de données d'image, tel que des données Windows Metafile, bitmap ou OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés connexes.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contient le texte d'une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Suppr  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indicateur signalant si l'élément est supprimé localement.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|FillStyle  <br/> |xsd: unsignedInt  <br/> ||ID de la feuille de style à partir de laquelle cette forme hérite de la mise en forme de remplissage.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID unique de l'élément au sein de son élément parent.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l'utilisateur.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l'utilisateur..  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|LineStyle  <br/> |xsd: unsignedInt  <br/> ||ID de la feuille de style à partir de laquelle cette forme hérite de la mise en forme de ligne.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Master  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de l'élément maître à partir duquel la forme hérite ses données.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|MasterShape  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de l'élément maître à partir duquel la forme hérite ses données.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Nom  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom de l'élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom universel de l'élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|TextStyle  <br/> |xsd: unsignedInt  <br/> ||ID de la feuille de style à partir de laquelle cette forme hérite de la mise en forme du texte.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Type  <br/> |xsd: Token  <br/> |facultatif  <br/> |Type d'une forme. Il peut s'agir de l'une des valeurs suivantes: Group, Shape, guide ou Foreign.  <br/> |Valeurs du type xsd: Token.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |facultatif  <br/> |GUID (globally unique identifier) affecté à la forme.  <br/> |Valeurs du type xsd: String.  <br/> |
   

