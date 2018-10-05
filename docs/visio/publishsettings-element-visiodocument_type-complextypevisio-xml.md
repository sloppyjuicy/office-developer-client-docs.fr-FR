---
title: Élément PublishSettings (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397211"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a>Élément PublishSettings (VisioDocument_Type, complexType) (« Visio XML »)

Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PublishedPage](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services.  <br/> |
|[RefreshableData](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |Indique si un objet recordset actualisable à l’aide de Visio Services.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

