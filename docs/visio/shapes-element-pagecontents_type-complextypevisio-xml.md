---
title: Élément de formes (PageContents_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contient une collection d’éléments de la forme.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397568"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a>Élément de formes (PageContents_Type, complexType) (« Visio XML »)

Contient une collection d’éléments de la forme.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |page # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MasterContents](mastercontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Spécifie des informations sur les formes dans une forme de base dans un dessin Web.  <br/> |
|[PageContents](pagecontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Spécifie des informations sur les formes dans une forme de base dans un dessin Web.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

