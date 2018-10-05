---
title: Élément AuthorList (Comments_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Spécifie les auteurs de commentaires dans un dessin.
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387740"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a>Élément AuthorList (Comments_Type, complexType) (« Visio XML »)

Spécifie les auteurs de commentaires dans un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Comments.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Comments](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |Spécifie les commentaires dans un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[AuthorEntry](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés qui identifient l’auteur d’un commentaire dans un dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

