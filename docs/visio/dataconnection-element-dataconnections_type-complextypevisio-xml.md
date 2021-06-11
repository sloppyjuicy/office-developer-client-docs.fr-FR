---
title: Élément DataConnection (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Extrait la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538402"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>Élément DataConnection (DataConnections_Type complexType) (Visio XML)

Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contient les **éléments DataConnection** du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |facultatif  <br/> |La valeur par défaut est false. Voir la section Remarques pour plus d'informations.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|Commande  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne de commande utilisée pour interroger la source de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|FileName  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom du fichier de connexion. Voir la section Remarques pour plus d'informations.  <br/> |Valeurs du type xsd:string.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom fourni par l’utilisateur pour la connexion de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID attribué par le Visio pour une connexion donnée, unique dans le document.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Délai d’attente en minutes lors de la tentative d’établissement d’une connexion avant la fin de la tentative.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

