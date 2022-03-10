---
title: Élément MentionsList (ModernCommentEntry_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie la liste des mentions dans un commentaire dans un dessin.
ms.openlocfilehash: 72962dd93ad8a639302db2ed5c7e0ebca237bd0e
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427041"
---
# <a name="mentionslist-element-moderncommententry_type-complextype-visio-xml"></a>Élément MentionsList (ModernCommentEntry_Type complexType) (Visio XML)

Spécifie la liste des mentions dans un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[MentionsList_Type](mentionslist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |moderncomments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="MentionsList" type="MentionsList_Type" minOccurs="0" maxOccurs="1" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ModernCommentEntry](moderncommententry-element-moderncommentslist_type-complextypevisio-xml.md) <br/> |[ModernCommentEntry_Type](moderncommententry_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et la liste des mentions dans un commentaire d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MentionEntry](mentionentry-element-mentionslist_type-complextypevisio-xml.md) <br/> |[MentionEntry_Type](mentionentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

Aucun.
  

