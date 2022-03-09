---
title: PersonsList_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: 41ff91fbb4466c5ce78660b814ae6bf75e39b68b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382469"
---
# <a name="personslist_type-complextype-visio-xml"></a>PersonsList_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
     <xs:complexType name="PersonsList_Type">
        <xs:sequence>
            <xs:element name="PersonEntry" type="PersonEntry_Type" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[PersonEntry](personentry-element-personslist_type-complextypevisio-xml.md) <br/> |[PersonEntry_Type](personentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

Aucun.
  


