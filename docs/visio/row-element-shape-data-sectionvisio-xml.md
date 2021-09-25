---
title: Row, élément (Shape Data Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Spécifie une entrée de données de forme pour associer des données à une forme.
ms.openlocfilehash: 3a52f456bf5e5639ccbed76d026ce151f5b1da8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554053"
---
# <a name="row-element-shape-data-section-visio-xml"></a>Row, élément (Shape Data Section) (Visio XML)

Spécifie une entrée de données de forme pour associer des données à une forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Forme Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Spécifie une entrée de données de forme pour associer des données à une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété des données de forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur à base un de la ligne. Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisé uniquement pour la section Geometry.  <br/> |Valeurs du type xsd:string.  <br/> |
   

