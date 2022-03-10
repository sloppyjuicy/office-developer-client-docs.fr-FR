---
title: Élément FaceName (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contient des informations sur une police.
ms.openlocfilehash: 05732c9774b88ac931ef8fedf26462dc761f1b2a
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427048"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>Élément FaceName (FaceNames_Type complexType) (Visio XML)

Contient des informations sur une police.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contient une collection **d’éléments FaceName** . |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd:string  <br/> |facultatif  <br/> |Jeux de caractères pris en charge de la police. |Valeurs du type xsd:string. |
|Flags  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Indicateurs qui indiquent les éléments suivants : police manquante, police par défaut, police asiatique, police complexe, police verticale et type de police. |Valeurs du type xsd:unsignedInt. |
|NameU  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom de la police sous la forme d’une chaîne Unicode UTF-16. ||
|Panos  <br/> |xsd:string  <br/> |facultatif  <br/> |Signature du volet de la police. Panose est un système de classification pour les polices qui les catégorise en fonction de leurs caractéristiques visuelles. |Valeurs du type xsd:string. |
|UnicodeRanges  <br/> |xsd:string  <br/> |facultatif  <br/> |Plages Unicode de la police prise en charge. |Valeurs du type xsd:string. |
   

