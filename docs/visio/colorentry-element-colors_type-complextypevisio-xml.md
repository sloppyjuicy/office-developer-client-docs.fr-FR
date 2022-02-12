---
title: Élément ColorEntry (Colors_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contient une entrée de tableau en couleurs.
ms.openlocfilehash: 1d2b4bf823f6f0fab9000aa8d96826b3acefaad3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788933"
---
# <a name="colorentry-element-colors_type-complextype-visio-xml"></a>Élément ColorEntry (Colors_Type complexType) (Visio XML)

Contient une entrée de tableau en couleurs.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ColorEntry_Type](colorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Colors](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Colors_Type](colors_type-complextypevisio-xml.md) <br/> |Contient le tableau de couleurs du document. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Index de base 0 de l’élément au sein de son élément parent. |Valeurs du type xsd:unsignedInt. |
|RVB  <br/> |xsd:string  <br/> |obligatoire  <br/> |Valeur hexadécimale de l’entrée de tableau de couleurs. |Valeurs du type xsd:string. |
   

