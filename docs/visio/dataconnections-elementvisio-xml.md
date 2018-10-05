---
title: Élément DataConnections (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contient les éléments DataConnection pour le document.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395027"
---
# <a name="dataconnections-element-visio-xml"></a>Élément DataConnections (« Visio XML »)

Contient les éléments **DataConnection** pour le document. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Connections.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataConnection](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |Analyse la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|NextID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’ID suivant disponible pour les nouvelles connexions.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

