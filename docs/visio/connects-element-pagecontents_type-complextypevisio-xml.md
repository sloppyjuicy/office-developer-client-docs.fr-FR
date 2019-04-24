---
title: Connects, élément (PageContents_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contient un élément Connect pour chaque connexion entre deux formes dans un dessin.
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318962"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a>Connects, élément (PageContents_Type complexType) ('Visio XML')

Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |page #. xml, Master #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MasterContents](mastercontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie les informations relatives aux formes d'une forme de base ou d'une page de dessin d'un dessin.  <br/> |
|[PageContents](pagecontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie les informations relatives aux formes d'une forme de base ou d'une page de dessin d'un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Connect](connect-element-connects_type-complextypevisio-xml.md) <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

