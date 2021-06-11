---
title: Élément FaceName (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contient des informations sur une police.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541014"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>Élément FaceName (FaceNames_Type complexType) (Visio XML)

Contient des informations sur une police.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contient une collection **d’éléments FaceName.**  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd:string  <br/> |facultatif  <br/> |Jeux de caractères pris en charge de la police.  <br/> |Valeurs du type xsd:string.  <br/> |
|Flags  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Indicateurs qui indiquent les éléments suivants : police manquante, police par défaut, police asiatique, police complexe, police verticale et type de police.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|NameU  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom de la police sous la forme d’une chaîne Unicode UTF-16.  <br/> ||
|Panos  <br/> |xsd:string  <br/> |facultatif  <br/> |Signature du volet de la police. Panose est un système de classification pour les polices qui les classe en fonction de leurs caractéristiques visuelles.  <br/> |Valeurs du type xsd:string.  <br/> |
|UnicodeRanges  <br/> |xsd:string  <br/> |facultatif  <br/> |Plages Unicode de la police prise en charge.  <br/> |Valeurs du type xsd:string.  <br/> |
   

