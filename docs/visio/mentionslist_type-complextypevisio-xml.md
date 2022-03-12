---
title: MentionsList_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: 574f09ec453cb6f161afc27a7b427c6cc0147792
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448264"
---
# <a name="mentionslist_type-complextype-visio-xml"></a>MentionsList_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

||Valeur |
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
         <xs:complexType name="MentionsList_Type">
        <xs:sequence>
            <xs:element name="MentionEntry" type="MentionEntry_Type" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[MentionEntry](mentionentry-element-mentionslist_type-complextypevisio-xml.md) <br/> |[MentionEntry_Type](mentionentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

Aucun.
  

