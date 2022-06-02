---
title: Élément ModernComments (VisioDocument_Type complexType) (Visio XML)
description: ModernComments (VisioDocument_Type complexType) spécifie les propriétés utilisées pour identifier le commentaire parent et les mentions présentes dans un commentaire de dessin.
ms.date: 02/18/2022
ms.openlocfilehash: 0b0a2acd9caaf9b53337b7ef81a674ccde13e8ee
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853810"
---
# <a name="moderncomments-element-visiodocument_type-complextype-visio-xml"></a>Élément ModernComments (VisioDocument_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier le commentaire parent des commentaires et des mentions présents dans les commentaires d’un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[ModernComments_Type](moderncomments_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |moderncomments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ModernComments" type="ModernComments_Type" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio. |
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[ModernCommentsList](moderncommentslist-element-moderncomments_type-complextypevisio-xml.md) <br/> |[ModernCommentsList_Type](moderncommentslist_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et la liste des mentions dans tous les commentaires d’un dessin.  |
   
### <a name="attributes"></a>Attributs

Aucun.
  

