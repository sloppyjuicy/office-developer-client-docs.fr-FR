---
title: SnapAngles, élément (Window_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5997f374-303a-92b6-6dd3-87ef81104af4
description: Contient une collection d’éléments SnapAngle.
ms.openlocfilehash: 09a975b280a99fdc2535503b587efdd2143cf18b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383099"
---
# <a name="snapangles-element-windowtype-complextype-visio-xml"></a>SnapAngles, élément (Window_Type, complexType) (« Visio XML »)

Contient une collection d’éléments **SnapAngle** . 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Représente une fenêtre ouverte dans une instance de Microsoft Visio.
  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[SnapAngle](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[SnapAngle_Type](snapangle_type-complextypevisio-xml.md) <br/> |Contient un flottante point nombre spécifiant un angle de composant logiciel enfichable en degrés.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

