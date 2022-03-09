---
title: Élément ModernCommentsList (ModernComments_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier le commentaire parent et les mentions présentes dans les commentaires d’un dessin.
ms.openlocfilehash: a699f8a309bf57be690bd770af42f6a9b37ebdaa
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382473"
---
# <a name="moderncommentslist-element-moderncomments_type-complextype-visio-xml"></a>Élément ModernCommentsList (ModernComments_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier le commentaire parent des commentaires et les mentions présents dans les commentaires d’un dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ModernCommentsList_Type](moderncommentslist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |moderncomments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="ModernCommentsList" type="ModernCommentsList_Type" minOccurs="0" maxOccurs="1" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[ModernComments](moderncomments-element-visiodocument_type-complextypevisio-xml.md) <br/> |[ModernComments_Type](moderncomments_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et les mentions présentes dans les commentaires d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[ModernCommentEntry](moderncommententry-element-moderncommentslist_type-complextypevisio-xml.md) <br/> |[ModernCommentEntry_Type](moderncommententry_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et la liste des mentions dans un commentaire d’un dessin. |
   
### <a name="attributes"></a>Attributs

Aucun.
  

