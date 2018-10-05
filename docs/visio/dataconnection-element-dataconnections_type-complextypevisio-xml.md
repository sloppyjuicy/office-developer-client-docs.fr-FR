---
title: DataConnection, élément (DataConnections_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Analyse la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399423"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>DataConnection, élément (DataConnections_Type, complexType) (« Visio XML »)

Analyse la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Connections.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contient les éléments **DataConnection** pour le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |La valeur par défaut est false. Pour plus d’informations, consultez la section Notes.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Commande  <br/> |XSD : String  <br/> |facultatif  <br/> |La chaîne de commande utilisée pour interroger la source de données.  <br/> |Valeurs du type xsd : String.  <br/> |
|ConnectionString  <br/> |XSD : String  <br/> |facultatif  <br/> |La chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données.  <br/> |Valeurs du type xsd : String.  <br/> |
|FileName  <br/> |XSD : String  <br/> |obligatoire  <br/> |Le nom du fichier de connexion. Pour plus d’informations, consultez la section Notes.  <br/> |Valeurs du type xsd : String.  <br/> |
|FriendlyName  <br/> |XSD : String  <br/> |facultatif  <br/> |Un nom fourni par l’utilisateur pour la connexion de données.  <br/> |Valeurs du type xsd : String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’ID affecté par Visio pour une connexion donnée, unique dans le document.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Timeout  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Le temps d’attente en minutes lors de la tentative d’établir une connexion avant l’abandon de la tentative.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

