---
title: ForeignData, élément (ShapeSheet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contient un BLOB codé MIME (Multipurpose Internet Mail Extensions) des données d’image, telles que les données OLE, bitmap ou métafichier Windows.
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382680"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData, élément (ShapeSheet_Type, complexType) (« Visio XML »)

Contient un BLOB codé MIME (Multipurpose Internet Mail Extensions) des données d’image, telles que les données OLE, bitmap ou métafichier Windows.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |page # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie une relation vers un composant contenant les données d’image.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD : double  <br/> |facultatif  <br/> |Spécifie le niveau de compression appliqué au fichier. Cet attribut est significatif que si les données étrangères sont un objet externe tramé, tel qu’un fichier DIB, JPG, PNG, TIFF ou GIF.  <br/> |Valeurs du type xsd : double.  <br/> |
|CompressionType  <br/> |XSD:Token  <br/> |facultatif  <br/> |Spécifie le type de compression appliqué au fichier. Cet attribut est significatif que si les données étrangères sont un objet externe tramé, tel qu’un fichier DIB, JPG, PNG, TIFF ou GIF  <br/> |Valeurs du type xsd:token.  <br/> |
|ExtentX  <br/> |XSD : double  <br/> |facultatif  <br/> |Spécifie la mesure horizontale du métafichier. Cet attribut est significatif que si les données étrangères sont un métafichier.  <br/> |Valeurs du type xsd : double.  <br/> |
|ExtentY  <br/> |XSD : double  <br/> |facultatif  <br/> |Spécifie l’étendue verticale du métafichier. Cet attribut est significatif que si les données étrangères sont un métafichier.  <br/> |Valeurs du type xsd : double.  <br/> |
|ForeignType  <br/> |XSD:Token  <br/> |obligatoire  <br/> |Indique un métafichier, EnhMetaFile, de type Bitmap, objet ou d’encre.  <br/> |Valeurs du type xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Spécifie le mode de mappage de métafichier. Cet attribut est significatif que si les données étrangères sont un métafichier.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD : double  <br/> |facultatif  <br/> |Spécifie la hauteur de l’objet en unités de page. Cet attribut est significatif que si les données étrangères sont un objet incorporé OLE2.  <br/> |Valeurs du type xsd : double.  <br/> |
|ObjectType  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Indicateur entier de type d’objet. Utilisé lorsque type étrangère est l’objet.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD : double  <br/> |facultatif  <br/> |Spécifie la largeur de l’objet en unités de page. Cet attribut est significatif que si les données étrangères sont un objet incorporé OLE2.  <br/> |Valeurs du type xsd : double.  <br/> |
|ShowAsIcon  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique s’il faut afficher ou non des données incorporées en tant qu’icône.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
   

