---
title: Élément PublishedPage (PublishSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 313cabbdd59930df67c807ee3c89df1a6e8c17a2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390981"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a>Élément PublishedPage (PublishSettings_Type, complexType) (« Visio XML »)

Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’identificateur d’une page de dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

