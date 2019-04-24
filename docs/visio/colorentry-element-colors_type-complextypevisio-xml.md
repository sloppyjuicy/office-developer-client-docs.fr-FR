---
title: Élément ColorEntry (complexType Colors_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contient une entrée de table de couleurs.
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358085"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a>Élément ColorEntry (complexType Colors_Type) ('Visio XML')

Contient une entrée de table de couleurs.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ColorEntry_Type](colorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Colors](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Colors_Type](colors_type-complextypevisio-xml.md) <br/> |Contient la table des couleurs du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |Index de base zéro de l'élément au sein de son élément parent.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|RVB  <br/> |xsd: String  <br/> |obligatoire  <br/> |Valeur hexadécimale de l'entrée de la table des couleurs.  <br/> |Valeurs du type xsd: String.  <br/> |
   

