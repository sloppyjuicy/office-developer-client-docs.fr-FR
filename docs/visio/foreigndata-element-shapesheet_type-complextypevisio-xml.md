---
title: Élément ForeignData (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contient un OBJET BLOB MIME (Multipurpose Internet Mail Extensions) codé de données d’image, telles que des données métafichier Windows, bitmap ou OLE.
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539841"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>Élément ForeignData (ShapeSheet_Type complexType) (Visio XML)

Contient un OBJET BLOB MIME (Multipurpose Internet Mail Extensions) codé de données d’image, telles que des données métafichier Windows, bitmap ou OLE.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une forme dans un **élément de forme de** groupe, page ou maître.   <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie une relation à une partie contenant les données d’image.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie le niveau de compression appliqué au fichier. Cet attribut n’est significatif que si les données étrangères sont un objet étranger basé sur raster, tel qu’un fichier DIB, JPG, PNG, TIFF ou GIF.  <br/> |Valeurs du type xsd:double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |facultatif  <br/> |Spécifie le type de compression appliqué au fichier. Cet attribut n’est significatif que si les données étrangères sont un objet étranger basé sur raster, tel qu’un fichier DIB, JPG, PNG, TIFF ou GIF  <br/> |Valeurs du type xsd:token.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie l’étendue horizontale du métafichier. Cet attribut n’est significatif que si les données étrangères sont un métafichier.  <br/> |Valeurs du type xsd:double.  <br/> |
|Extenty  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie l’étendue verticale du métafichier. Cet attribut n’est significatif que si les données étrangères sont un métafichier.  <br/> |Valeurs du type xsd:double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |obligatoire  <br/> |Indique le type metafile, EnhMetaFile, Bitmap, Object ou Ink.  <br/> |Valeurs du type xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Spécifie le mode de mappage de métafichier. Cet attribut n’est significatif que si les données étrangères sont un métafichier.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie la hauteur de l’objet en unités de page. Cet attribut n’est significatif que si les données étrangères sont un objet incorporé OLE2.  <br/> |Valeurs du type xsd:double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Un indicateur de type objet d’un nombre-nombre. Utilisé lorsque le type étranger est un objet.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie la largeur de l’objet en unités de page. Cet attribut n’est significatif que si les données étrangères sont un objet incorporé OLE2.  <br/> |Valeurs du type xsd:double.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique s’il faut afficher ou non les données incorporées sous forme d’icône.  <br/> |Valeurs du type xsd:boolean.  <br/> |
   

