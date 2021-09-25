---
title: Élément DataConnections (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contient les éléments DataConnection du document.
ms.openlocfilehash: 854da46d8536cce8776f2a4b9eb8a28e50ea4588
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563076"
---
# <a name="dataconnections-element-visio-xml"></a>Élément DataConnections (Visio XML)

Contient les **éléments DataConnection** du document. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataConnection](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|NextID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID disponible suivant pour les nouvelles connexions.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

