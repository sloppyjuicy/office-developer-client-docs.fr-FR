---
title: Élément ModernComments (VisioDocument_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier le commentaire parent et les mentions présentes dans les commentaires d’un dessin.
ms.openlocfilehash: 5311c69b714b09895f662c79f26fc33ff7d4af8d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382476"
---
# <a name="moderncomments-element-visiodocument_type-complextype-visio-xml"></a>Élément ModernComments (VisioDocument_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier le commentaire parent des commentaires et les mentions présents dans les commentaires d’un dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ModernComments_Type](moderncomments_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |moderncomments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ModernComments" type="ModernComments_Type" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio document. |
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[ModernCommentsList](moderncommentslist-element-moderncomments_type-complextypevisio-xml.md) <br/> |[ModernCommentsList_Type](moderncommentslist_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et la liste des mentions dans tous les commentaires d’un dessin.  |
   
### <a name="attributes"></a>Attributs

Aucun.
  

