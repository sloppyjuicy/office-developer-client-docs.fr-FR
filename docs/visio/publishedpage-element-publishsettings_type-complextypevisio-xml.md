---
title: Élément PublishedPage (PublishSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Spécifie si une page de dessin est consultable dans le navigateur à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 71af8156b438a2f85f88a8bd5f41b8d39d2c0126
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788800"
---
# <a name="publishedpage-element-publishsettings_type-complextype-visio-xml"></a>Élément PublishedPage (PublishSettings_Type complexType) (Visio XML)

Spécifie si une page de dessin est consultable dans le navigateur à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Spécifie les paramètres utilisés lorsque le diagramme est ouvert à l’aide de Visio Services. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Identificateur d’une page de dessin. |Valeurs du type xsd:unsignedInt. |
   

