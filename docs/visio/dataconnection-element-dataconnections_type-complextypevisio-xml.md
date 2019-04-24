---
title: DataConnection, élément (DataConnections_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Extrait la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344624"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>DataConnection, élément (DataConnections_Type complexType) ('Visio XML')

Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Connections. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contient les éléments **DataConnection** pour le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |La valeur par défaut est false. Voir la section Remarques pour plus d'informations.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|Command  <br/> |xsd: String  <br/> |facultatif  <br/> |Chaîne de commande utilisée pour interroger la source de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|ConnectionString  <br/> |xsd: String  <br/> |facultatif  <br/> |Chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|FileName  <br/> |xsd: String  <br/> |obligatoire  <br/> |Nom du fichier de connexion. Voir la section Remarques pour plus d'informations.  <br/> |Valeurs du type xsd: String.  <br/> |
|FriendlyName  <br/> |xsd: String  <br/> |facultatif  <br/> |Un nom fourni par l'utilisateur pour la connexion de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID attribué par Visio pour une connexion donnée, unique dans le document.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Timeout  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Temps d'attente en minutes lors d'une tentative d'établissement d'une connexion avant la fin de la tentative.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

