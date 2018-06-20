---
title: Nom de la police, élément (FaceNames_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contient des informations sur une police.
ms.openlocfilehash: 8a66d5294e239e4540939cc7053e1f67a777144d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788578"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Nom de la police, élément (FaceNames_Type, complexType) (« Visio XML »)

Contient des informations sur une police.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contient une collection d’éléments de **nom de la police** .  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Jeux de caractères  <br/> |XSD : String  <br/> |facultatif  <br/> |Les jeux de caractères pris en charge de la police.  <br/> |Valeurs du type xsd : String.  <br/> |
|Indicateurs  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Indicateurs qui influencent les éléments suivants : manque de police, la police par défaut, police de caractères asiatiques, police complexe, police verticale et type de police.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|NameU  <br/> |XSD : String  <br/> |obligatoire  <br/> |Le nom de la police sous forme de chaîne Unicode UTF-16.  <br/> ||
|Panos  <br/> |XSD : String  <br/> |facultatif  <br/> |La signature panose la police. Panose est un système de classification de polices qui les classe en fonction de leurs caractéristiques visuelles.  <br/> |Valeurs du type xsd : String.  <br/> |
|UnicodeRanges  <br/> |XSD : String  <br/> |facultatif  <br/> |Les plages Unicode pris en charge de la police.  <br/> |Valeurs du type xsd : String.  <br/> |
   

