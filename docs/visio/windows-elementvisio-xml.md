---
title: Élément de Windows (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contient les éléments de la fenêtre d’un document.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386802"
---
# <a name="windows-element-visio-xml"></a>Élément de Windows (« Visio XML »)

Contient les éléments de la **fenêtre** d’un document. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Représente une fenêtre ouverte dans une instance de Microsoft Visio.
  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Représente la hauteur d’une zone d’affichage  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ClientWidth  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Représente la largeur d’une zone d’affichage  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
   

