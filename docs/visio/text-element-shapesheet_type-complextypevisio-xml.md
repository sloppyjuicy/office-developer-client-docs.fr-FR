---
title: Élément Text (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contient le texte d’une forme.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541924"
---
# <a name="text-element-shapesheet_type-complextype-visio-xml"></a>Élément Text (ShapeSheet_Type complexType) (Visio XML)

Contient le texte d’une forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
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
|[cp](cp-element-text_type-complextypevisio-xml.md) <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |Marque le début d’une exécute de propriétés de caractères mise en forme en fonction de l’élément Char correspondant.  <br/> |
|[fld](fld-element-text_type-complextypevisio-xml.md) <br/> |[fld_Type](fld_type-complextypevisio-xml.md) <br/> |Indique un point d’insertion de champ de texte pour l’élément Field correspondant.  <br/> |
|[pp](pp-element-text_type-complextypevisio-xml.md) <br/> |[pp_Type](pp_type-complextypevisio-xml.md) <br/> |Spécifie le début d’une exécute de propriétés de paragraphe.  <br/> |
|[tp](tp-element-text_type-complextypevisio-xml.md) <br/> |[tp_Type](tp_type-complextypevisio-xml.md) <br/> |Spécifie le début d’une exécuter les propriétés d’onglets.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

