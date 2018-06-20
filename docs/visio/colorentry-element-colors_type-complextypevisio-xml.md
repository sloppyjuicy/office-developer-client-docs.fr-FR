---
title: Élément ColorEntry (Colors_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contient une entrée de table de couleur.
ms.openlocfilehash: 934680b36428dd272d383ce421e86ae6d5c707cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788283"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a>Élément ColorEntry (Colors_Type, complexType) (« Visio XML »)

Contient une entrée de table de couleur.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ColorEntry_Type](colorentry_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Couleurs](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Colors_Type](colors_type-complextypevisio-xml.md) <br/> |Contient la table des couleurs du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Index de base zéro de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RVB  <br/> |XSD : String  <br/> |obligatoire  <br/> |La valeur hexadécimale de l’entrée de table de couleur.  <br/> |Valeurs du type xsd : String.  <br/> |
   

