---
title: Windows’élément (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contient les éléments Window d’un document.
ms.openlocfilehash: f835ce3a8f9c1af2735732fa6074cc4c8e9fbcb8
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634260"
---
# <a name="windows-element-visio-xml"></a>Windows’élément (Visio XML)

Contient les **éléments Window** d’un document. 
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Représente une fenêtre ouverte dans une instance de Microsoft Visio. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Représente la dimension de hauteur d’une zone d’affichage  <br/> |Valeurs du type xsd:unsignedShort. |
|ClientWidth  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Représente la dimension largeur d’une zone d’affichage  <br/> |Valeurs du type xsd:unsignedShort. |
   

