---
title: Élément Connects (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contient un Connecter pour chaque connexion entre deux formes dans un dessin.
ms.openlocfilehash: 9d9e009d1deeec997b20cf4084f1f8d1b15fa1fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613008"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a>Élément Connects (PageContents_Type complexType) (Visio XML)

Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MasterContents](mastercontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Spécifie les informations sur les formes d’une forme de base ou d’une page de dessin d’un dessin.  <br/> |
|[PageContents](pagecontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Spécifie les informations sur les formes d’une forme de base ou d’une page de dessin d’un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Connect](connect-element-connects_type-complextypevisio-xml.md) <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

