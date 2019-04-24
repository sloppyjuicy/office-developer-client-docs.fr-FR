---
title: Élément de ligne (section champ) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
ms.openlocfilehash: 578269b9bcb2a85db2145f1bccafd3c3cff91936
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358492"
---
# <a name="row-element-field-section-visio-xml"></a>Élément de ligne (section champ) ('Visio XML')

Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Master #. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l'aide de la boîte de dialogue champ  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Suppr  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si une ligne qui serait normalement héritée d'une forme de base a été supprimée.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l'identificateur de base 1 de la ligne. Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L'attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs. Une ligne ne peut avoir qu'un des attributs IX ou N.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd: String.  <br/> |
|N  <br/> |xsd: String  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant de la langue de la ligne. L'attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, hyperLink et ActionTag. Une ligne ne peut avoir qu'un des attributs IX ou N.  <br/> |Valeurs du type xsd: String.  <br/> |
|T  <br/> |xsd: String  <br/> |facultatif  <br/> |Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie. L'attribut T est utilisé uniquement pour la section Geometry.  <br/> |Valeurs du type xsd: String.  <br/> |
   

