---
title: Élément CommentEntry (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.
ms.openlocfilehash: 39b3f6808aba401006bd1365fbcfcaed59d9e86c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772892"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a>Élément CommentEntry (CommentList_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Spécifie les commentaires d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur basée sur un qui identifie l’auteur. |Valeurs du type xsd:unsignedInt. |
|CommentID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur unique qui identifie le commentaire dans une page de dessin. |Valeurs du type xsd:unsignedInt. |
|Date  <br/> |xsd:dateTime  <br/> |obligatoire  <br/> |Indique quand un commentaire a été créé. |Valeurs du type xsd:dateTime. |
|Terminé  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie l’état actuel du commentaire. |Valeurs du type xsd:boolean. |
|EditDate  <br/> |xsd:dateTime  <br/> |facultatif  <br/> |Indique quand un commentaire a été modifié pour la dernière fois. |Valeurs du type xsd:dateTime. |
|PageID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur qui identifie la page de dessin sur qui se trouve le commentaire. |Valeurs du type xsd:unsignedInt. |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Valeur qui identifie la forme sur quelle forme se trouve le commentaire. Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin. |Valeurs du type xsd:unsignedInt. |
   

