---
title: Se connecter, élément (Connects_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.\n"
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399318"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Se connecter, élément (Connects_Type, complexType) (« Visio XML »)


			Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.

  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |page # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD : String  <br/> |facultatif  <br/> |La cellule à l’origine une connexion.  <br/> |Valeurs du type xsd : String.  <br/> |
|FromPart  <br/> |XSD : int  <br/> |facultatif  <br/> |La partie de la forme à partir de laquelle une connexion.  <br/> |Valeurs du type xsd : int.  <br/> |
|FromSheet  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’ID de la forme à partir de laquelle une connexion ou proviennent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ToCell  <br/> |XSD : String  <br/> |facultatif  <br/> |La cellule avec laquelle une connexion est établie.  <br/> |Valeurs du type xsd : String.  <br/> |
|ToPart  <br/> |XSD : int  <br/> |facultatif  <br/> |La partie de la forme avec laquelle une connexion est établie.  <br/> |Valeurs du type xsd : int.  <br/> |
|ToSheet  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’ID de la forme à laquelle une ou plusieurs connexions sont effectuées.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

