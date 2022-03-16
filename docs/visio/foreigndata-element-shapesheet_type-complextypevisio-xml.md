---
title: Élément ForeignData (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contient un OBJET BLOB MIME (Multipurpose Internet Mail Extensions) codé de données d’image, telles que Windows métafichier, bitmap ou données OLE.
ms.openlocfilehash: 507dd9871def50db7076877745fa6fe0976c773c
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508102"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>Élément ForeignData (ShapeSheet_Type complexType) (Visio XML)

Contient un OBJET BLOB MIME (Multipurpose Internet Mail Extensions) codé de données d’image, telles que Windows métafichier, bitmap ou données OLE.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une forme dans un **élément Master**, **Page** ou Group Shape. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie une relation à une partie contenant les données d’image. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie le niveau de compression appliqué au fichier. Cet attribut n’est significatif que si les données étrangères sont un objet étranger basé sur raster, tel qu’un fichier DIB, JPG, PNG, TIFF ou GIF. |Valeurs du type xsd:double. |
|CompressionType  <br/> |xsd:token  <br/> |facultatif  <br/> |Spécifie le type de compression appliqué au fichier. Cet attribut n’est significatif que si les données étrangères sont un objet étranger basé sur raster, tel qu’un fichier DIB, JPG, PNG, TIFF ou GIF  <br/> |Valeurs du type xsd:token. |
|ExtentX  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie l’étendue horizontale du métafichier. Cet attribut n’est significatif que si les données étrangères sont un métafichier. |Valeurs du type xsd:double. |
|Extenty  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie l’étendue verticale du métafichier. Cet attribut n’est significatif que si les données étrangères sont un métafichier. |Valeurs du type xsd:double. |
|ForeignType  <br/> |xsd:token  <br/> |obligatoire  <br/> |Indique le type metafile, EnhMetaFile, Bitmap, Object ou Ink. |Valeurs du type xsd:token. |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Spécifie le mode de mappage de métafichier. Cet attribut n’est significatif que si les données étrangères sont un métafichier. |Valeurs du type xsd:unsignedShort. |
|ObjectHeight  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie la hauteur de l’objet en unités de page. Cet attribut n’est significatif que si les données étrangères sont un objet incorporé OLE2. |Valeurs du type xsd:double. |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Un indicateur de type objet d’un nombre-nombre. Utilisé lorsque le type étranger est un objet. |Valeurs du type xsd:unsignedInt. |
|ObjectWidth  <br/> |xsd:double  <br/> |facultatif  <br/> |Spécifie la largeur de l’objet en unités de page. Cet attribut n’est significatif que si les données étrangères sont un objet incorporé OLE2. |Valeurs du type xsd:double. |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique s’il faut afficher ou non les données incorporées sous forme d’icône. |Valeurs du type xsd:boolean. |
   

