---
title: Élément MentionEntry (MentionsList_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier une mention dans un commentaire dans un dessin.
ms.openlocfilehash: 1864a539f987a59adda3cf89d05dbb1dff8b34c8
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426754"
---
# <a name="mentionentry-element-mentionslist_type-complextype-visio-xml"></a>Élément MentionEntry (MentionsList_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier une mention dans un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[MentionEntry_Type](mentionentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |moderncomments.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="MentionEntry" type="MentionEntry_Type" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MentionsList](mentionslist-element-moderncommententry_type-complextypevisio-xml.md) <br/> |[MentionsList_Type](mentionslist_type-complextypevisio-xml.md) <br/> |Spécifie la liste des mentions dans un commentaire dans un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|MentionCheckSum  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur de hachage de la partie du texte du commentaire à partir de l’index 0 ou de l’index de fin de mention précédente jusqu’à l’index de mention actuel|Valeurs du type xsd:unsignedInt. |
|MentionPersonID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> | Une valeur basée sur un qui identifie la personne|Valeurs du type xsd:unsignedInt. |
|MentionID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur unique qui identifie une mention dans les commentaires d’un dessin|Valeurs du type xsd:unsignedInt. |
|StartIndex  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Publication de départ d’une mention dans un commentaire |Valeurs du type xsd:unsignedInt. |
|Longueur  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> | Longueur de la mention dans un commment|Valeurs du type xsd:unsignedInt. |
   

