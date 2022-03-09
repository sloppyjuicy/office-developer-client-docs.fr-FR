---
title: Élément MentionEntry (MentionsList_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier une mention dans un commentaire dans un dessin.
ms.openlocfilehash: bea904f4efb1b457f2d46598c42fd19e415af397
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371623"
---
# <a name="mentionentry-element-mentionslist_type-complextype-visio-xml"></a>Élément MentionEntry (MentionsList_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier une mention dans un commentaire dans un dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

|**Élément**|**Type (Type)**|**Description**|
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
   

