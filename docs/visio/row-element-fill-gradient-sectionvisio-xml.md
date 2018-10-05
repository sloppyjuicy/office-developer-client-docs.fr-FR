---
title: Row, élément (remplissage dégradé Section) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.
ms.openlocfilehash: 55ec3b58f57d1fb008825c1a5a4156e5aec59552
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393774"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a>Row, élément (remplissage dégradé Section) (« Visio XML »)

Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.XML, master # .xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPPR.  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur de base 1 pour la ligne. Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets. Une ligne peut être un des attributs IX ou N.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd : String.  <br/> |
|N  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag. Une ligne peut être un des attributs IX ou N.  <br/> |Valeurs du type xsd : String.  <br/> |
|T  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisée uniquement pour la section Geometry.  <br/> |Valeurs du type xsd : String.  <br/> |
   

