---
title: Élément AuthorEntry (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.
ms.openlocfilehash: e8681a0425f7749924358ee088fd6499456b926d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578234"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a>Élément AuthorEntry (AuthorList_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Spécifie les auteurs d’un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur basée sur une valeur qui identifie l’auteur.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Initials  <br/> |xsd:string  <br/> |facultatif  <br/> |Initiales de l’auteur.  <br/> |Valeurs du type xsd:string.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’auteur.  <br/> |Valeurs du type xsd:string.  <br/> |
|ResolutionID  <br/> |xsd:string  <br/> |facultatif  <br/> |Identificateur unique de l’auteur.  <br/> |Valeurs du type xsd:string.  <br/> |
   

