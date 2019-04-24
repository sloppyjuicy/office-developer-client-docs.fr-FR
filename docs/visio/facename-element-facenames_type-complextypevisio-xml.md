---
title: Élément FaceName (complexType FaceNames_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contient des informations sur une police.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322602"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Élément FaceName (complexType FaceNames_Type) ('Visio XML')

Contient des informations sur une police.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contient une collection d'éléments **FaceName** .  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Jeux de caractères  <br/> |xsd: String  <br/> |facultatif  <br/> |Jeux de caractères pris en charge de la police.  <br/> |Valeurs du type xsd: String.  <br/> |
|Flags  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Indicateurs qui indiquent les éléments suivants: police manquante, police par défaut, police asiatique, police complexe, police verticale et type de police.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|NameU  <br/> |xsd: String  <br/> |obligatoire  <br/> |Nom de la police sous la forme d'une chaîne Unicode UTF-16.  <br/> ||
|Panos  <br/> |xsd: String  <br/> |facultatif  <br/> |Signature Panose de la police. PaNose est un système de classification pour les polices qui les classe par rapport à leurs caractéristiques visuelles.  <br/> |Valeurs du type xsd: String.  <br/> |
|UnicodeRanges  <br/> |xsd: String  <br/> |facultatif  <br/> |Plages Unicode prises en charge de la police.  <br/> |Valeurs du type xsd: String.  <br/> |
   

