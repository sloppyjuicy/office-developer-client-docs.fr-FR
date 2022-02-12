---
title: Élément AuthorEntry (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.
ms.openlocfilehash: cb827b0da6e5f2ef31306061e5e7a62c587530ab
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787491"
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Spécifie les auteurs d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur basée sur un qui identifie l’auteur. |Valeurs du type xsd:unsignedInt. |
|Initials  <br/> |xsd:string  <br/> |facultatif  <br/> |Initiales de l’auteur. |Valeurs du type xsd:string. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’auteur. |Valeurs du type xsd:string. |
|ResolutionID  <br/> |xsd:string  <br/> |facultatif  <br/> |Identificateur unique de l’auteur. |Valeurs du type xsd:string. |
   

