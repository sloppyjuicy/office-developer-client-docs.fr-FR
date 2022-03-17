---
title: Élément Persons (VisioDocument_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier les personnes mentionnées dans les commentaires d’un dessin
ms.openlocfilehash: c72a2c325d369cc111938e86e5f7f55ba5a73c14
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521868"
---
# <a name="persons-element-visiodocument_type-complextype-visio-xml"></a>Élément Persons (VisioDocument_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier les personnes mentionnées dans les commentaires d’un dessin
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Persons_Type](persons_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |persons.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Persons" type="Persons_Type" minOccurs="0" maxOccurs="1" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio document. |
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PersonsList](personslist-element-persons_type-complextypevisio-xml.md) <br/> |[PersonsList_Type](personslist_type-complextypevisio-xml.md) <br/> |Spécifie la liste des personnes mentionnées dans les commentaires d’un dessin. |
   
### <a name="attributes"></a>Attributs

Aucun.
  

