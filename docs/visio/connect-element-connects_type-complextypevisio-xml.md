---
title: Connect, élément (Connects_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346507"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Connect, élément (Connects_Type complexType) ('Visio XML')

Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |page #. xml, Master #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd: String  <br/> |facultatif  <br/> |Cellule à l'origine de la connexion.  <br/> |Valeurs du type xsd: String.  <br/> |
|FromPart  <br/> |xsd: int  <br/> |facultatif  <br/> |Partie d'une forme à l'origine d'une connexion.  <br/> |Valeurs du type xsd: int.  <br/> |
|FromSheet  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID de la forme à partir de laquelle une ou des connexions sont à l'origine de la connexion.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ToCell  <br/> |xsd: String  <br/> |facultatif  <br/> |Cellule vers laquelle une connexion est établie.  <br/> |Valeurs du type xsd: String.  <br/> |
|ToPart  <br/> |xsd: int  <br/> |facultatif  <br/> |Partie d'une forme à laquelle une connexion est établie.  <br/> |Valeurs du type xsd: int.  <br/> |
|ToSheet  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID de la forme à laquelle une ou plusieurs connexions sont établies.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

