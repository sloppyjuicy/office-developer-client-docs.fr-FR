---
title: Élément CommentEntry (CommentList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397043"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Élément CommentEntry (CommentList_Type, complexType) (« Visio XML »)

Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Comments.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Spécifie les commentaires dans un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Une valeur de base 1 qui identifie l’auteur.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|CommentID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Valeur unique qui identifie le commentaire dans une page de dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Date  <br/> |XSD : DateTime  <br/> |obligatoire  <br/> |Spécifie si un commentaire a été créé.  <br/> |Valeurs du type xsd : DateTime.  <br/> |
|Terminé  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie l’état actuel du commentaire.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|EditDate  <br/> |XSD : DateTime  <br/> |facultatif  <br/> |Spécifie si un commentaire a été modifié pour la dernière.  <br/> |Valeurs du type xsd : DateTime.  <br/> |
|PageID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Une valeur qui identifie la page de dessin le commentaire est activé.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Une valeur qui identifie la forme le commentaire est sur. Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

