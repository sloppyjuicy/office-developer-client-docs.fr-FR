---
title: Connecter’élément (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
ms.openlocfilehash: 57b9e31924540cbc1b06d225661193d362e6f95b
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427174"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Connecter’élément (Connects_Type complexType) (Visio XML)

Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |facultatif  <br/> |Cellule d’où provient une connexion. |Valeurs du type xsd:string. |
|FromPart  <br/> |xsd:int  <br/> |facultatif  <br/> |Partie d’une forme d’où provient une connexion. |Valeurs du type xsd:int. |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de la forme d’où provient une ou plusieurs connexions. |Valeurs du type xsd:unsignedInt. |
|ToCell  <br/> |xsd:string  <br/> |facultatif  <br/> |Cellule à laquelle une connexion est réalisée. |Valeurs du type xsd:string. |
|ToPart  <br/> |xsd:int  <br/> |facultatif  <br/> |Partie d’une forme à laquelle une connexion est établir. |Valeurs du type xsd:Int. |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de la forme à laquelle une ou plusieurs connexions sont réalisées. |Valeurs du type xsd:unsignedInt. |
   

