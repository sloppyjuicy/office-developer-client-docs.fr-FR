---
title: Élément ModernCommentEntry (ModernCommentsList_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier le commentaire parent et la liste des mentions dans un commentaire d’un dessin.
ms.openlocfilehash: 118db7279f1e1ad56b948b5eae06f7b040c2c782
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634792"
---
# <a name="moderncommententry-element-moderncommentslist_type-complextype-visio-xml"></a>Élément ModernCommentEntry (ModernCommentsList_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier le commentaire parent d’un commentaire et la liste des mentions présentes dans un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[ModernCommentEntry_Type](moderncommententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |moderncomments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="ModernCommentEntry" type="ModernCommentEntry_Type" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ModernCommentsList](moderncommentslist-element-moderncomments_type-complextypevisio-xml.md) <br/> |[ModernCommentsList_Type](moderncommentslist_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et la liste des mentions dans tous les commentaires d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MentionsList](mentionslist-element-moderncommententry_type-complextypevisio-xml.md) <br/> |[MentionsList_Type](mentionslist_type-complextypevisio-xml.md) <br/> |Spécifie la liste des mentions dans un commentaire dans un dessin. |
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CommentID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur unique qui identifie le commentaire dans le dessin. |Valeurs du type xsd:unsignedInt. |
|ParentID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Valeur unique qui identifie le commentaire parent dans le dessin. |Valeurs du type xsd:unsignedInt. |

