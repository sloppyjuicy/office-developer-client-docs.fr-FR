---
title: Élément CommentEntry (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540111"
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Spécifie les commentaires d’un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur basée sur un qui identifie l’auteur.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur unique qui identifie le commentaire dans une page de dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Date  <br/> |xsd:dateTime  <br/> |obligatoire  <br/> |Indique quand un commentaire a été créé.  <br/> |Valeurs du type xsd:dateTime.  <br/> |
|Terminé  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie l’état actuel du commentaire.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |facultatif  <br/> |Indique quand un commentaire a été modifié pour la dernière fois.  <br/> |Valeurs du type xsd:dateTime.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur qui identifie la page de dessin sur qui se trouve le commentaire.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Valeur qui identifie la forme sur quelle forme se trouve le commentaire. Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

