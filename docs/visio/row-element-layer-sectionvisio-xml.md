---
title: Row, élément (Section Layer) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contient des éléments qui définissent une couche unique et à ses propriétés pour une page.
ms.openlocfilehash: 2aff1666f5a2cb87ed10b76e0facdb19a4278c89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396840"
---
# <a name="row-element-layer-section-visio-xml"></a>Row, élément (Section Layer) (« Visio XML »)

Contient des éléments qui définissent une couche unique et à ses propriétés pour une page.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.XML, pages.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une couche unique et à ses propriétés pour une page.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’un calque ou ses propriétés pour une page.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPPR.  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur de base 1 pour la ligne. Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets. Une ligne peut être un des attributs IX ou N.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd : String.  <br/> |
|N  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag. Une ligne peut être un des attributs IX ou N.  <br/> |Valeurs du type xsd : String.  <br/> |
|T  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisée uniquement pour la section Geometry.  <br/> |Valeurs du type xsd : String.  <br/> |
   

