---
title: Connecter’élément (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
ms.openlocfilehash: 933a58a4afece3798e419f1a483b00f0d823961a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560010"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Connecter’élément (Connects_Type complexType) (Visio XML)

Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |facultatif  <br/> |Cellule d’où provient une connexion.  <br/> |Valeurs du type xsd:string.  <br/> |
|FromPart  <br/> |xsd:int  <br/> |facultatif  <br/> |Partie d’une forme d’où provient une connexion.  <br/> |Valeurs du type xsd:int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de la forme d’où provient une ou plusieurs connexions.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd:string  <br/> |facultatif  <br/> |Cellule à laquelle une connexion est réalisée.  <br/> |Valeurs du type xsd:string.  <br/> |
|ToPart  <br/> |xsd:int  <br/> |facultatif  <br/> |Partie d’une forme à laquelle une connexion est établir.  <br/> |Valeurs du type xsd:Int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de la forme à laquelle une ou plusieurs connexions sont réalisées.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

