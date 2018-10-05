---
title: Élément de forme (Shapes_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contient des éléments qui définissent une forme dans une forme de base, Page ou élément de forme de groupe.
ms.openlocfilehash: 6308b8dd21c92f6ced9ea7f03ec8aa85773fa2bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399679"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Élément de forme (Shapes_Type, complexType) (« Visio XML »)

Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |page # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
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
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contient un BLOB codé MIME (Multipurpose Internet Mail Extensions) des données d’image, telles que les données OLE, bitmap ou métafichier Windows.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés connexes.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Spécifie une collection de formes.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contient le texte d’une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPPR.  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indicateur signalant si l’élément est supprimé localement.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|FillStyle  <br/> |XSD:unsignedInt  <br/> ||ID de la feuille de style à partir de laquelle cette forme hérite de la mise en forme du remplissage.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IsCustomNameU  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur...  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> ||ID de la feuille de style à partir de laquelle cette forme hérite de la mise en forme du trait.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |L’ID de la forme de base élément à partir de laquelle la forme hérite ses données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |L’ID de la forme de base élément à partir de laquelle la forme hérite ses données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Le nom de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> ||ID de la feuille de style à partir de laquelle cette forme hérite de la mise en forme de texte.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Type  <br/> |XSD:Token  <br/> |facultatif  <br/> |Le type d’une forme. Il peut être une des valeurs suivantes : groupe, une forme, Guide ou externe.  <br/> |Valeurs du type xsd:token.  <br/> |
|UniqueID  <br/> |XSD : String  <br/> |facultatif  <br/> |Un GUID (identificateur global unique) affecté à la forme.  <br/> |Valeurs du type xsd : String.  <br/> |
   

