---
title: Persons_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: f02f429018730f692fac366f928016c04b83fc6c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371660"
---
# <a name="persons_type-complextype-visio-xml"></a>Persons_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
            <xs:complexType name="Persons_Type">
        <xs:sequence>
            <xs:element name="PersonsList" type="PersonsList_Type" minOccurs="0" maxOccurs="1" />
        </xs:sequence>
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[PersonsList](personslist-element-persons_type-complextypevisio-xml.md) <br/> |[PersonsList_Type](personslist_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier les personnes mentionnées dans les commentaires d’un dessin.|
   
### <a name="attributes"></a>Attributs

Aucun.
   

