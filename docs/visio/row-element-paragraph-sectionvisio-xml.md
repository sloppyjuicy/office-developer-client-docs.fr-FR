---
title: Élément de ligne (section paragraphe) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 00ecaa82-3b40-24cc-91c0-b2562e92161d
description: Indique les attributs de mise en forme de paragraphe du texte de la forme, tels que les retraits, l'interligne, les puces et l'alignement horizontal des paragraphes.
ms.openlocfilehash: 48d32f3a0712e2ed3110ced545d5b946f147d755
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540818"
---
# <a name="row-element-paragraph-section-visio-xml"></a>Élément de ligne (section paragraphe) (XML Visio)

Indique les attributs de mise en forme de paragraphe du texte de la forme, tels que les retraits, l'interligne, les puces et l'alignement horizontal des paragraphes.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. xml, Master #. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="ParagraphRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Indique les attributs de mise en forme de paragraphe du texte de la forme, tels que les retraits, l'interligne, les puces et l'alignement horizontal des paragraphes.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Suppr  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si une ligne qui serait normalement héritée d’une forme de base a été supprimée.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur de base 1 de la ligne. Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd: String.  <br/> |
|N  <br/> |xsd: String  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, HYPERLINK et ActionTag. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd: String.  <br/> |
|T  <br/> |xsd: String  <br/> |facultatif  <br/> |Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisé uniquement pour la section Geometry.  <br/> |Valeurs du type xsd: String.  <br/> |
   

