---
title: Élément DataConnection (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Extrait la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 29ba4de92403d33922a37ed05c8203c6c885fbf0
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448747"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>Élément DataConnection (DataConnections_Type complexType) (Visio XML)

Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML. 
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contient les **éléments DataConnection** du document. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |facultatif  <br/> |La valeur par défaut est false. Voir la section Remarques pour plus d'informations. |Valeurs du type xsd:boolean. |
|Commande  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne de commande utilisée pour interroger la source de données. |Valeurs du type xsd:string. |
|ConnectionString  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données. |Valeurs du type xsd:string. |
|FileName  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom du fichier de connexion. Voir la section Remarques pour plus d'informations. |Valeurs du type xsd:string. |
|FriendlyName  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom fourni par l’utilisateur pour la connexion de données. |Valeurs du type xsd:string. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID attribué par Visio pour une connexion donnée, unique dans le document. |Valeurs du type xsd:unsignedInt. |
|Timeout  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Délai d’attente en minutes lors de la tentative d’établissement d’une connexion avant la fin de la tentative. |Valeurs du type xsd:unsignedInt. |
   

