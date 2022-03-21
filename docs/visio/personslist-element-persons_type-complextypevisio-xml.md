---
title: Élément PersonsList (Persons_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie la liste des personnes mentionnées dans les commentaires d’un dessin.
ms.openlocfilehash: db7cf1a0f837104f6ccf6830731c6a5dc1a4aaac
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631686"
---
# <a name="personslist-element-persons_type-complextype-visio-xml"></a>Élément PersonsList (Persons_Type complexType) (Visio XML)

Spécifie la liste des personnes mentionnées dans les commentaires d’un dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[PersonsList_Type](personslist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |persons.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="PersonsList" type="PersonsList_Type" minOccurs="0" maxOccurs="1" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Personnes](persons-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Persons_Type](persons_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier les personnes mentionnées dans tous les commentaires d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PersonEntry](personentry-element-personslist_type-complextypevisio-xml.md) <br/> |[PersonEntry_Type](personentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

Aucun.
  

