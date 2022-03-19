---
title: ModernComments_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: 8cc5e40afe2c3af02b16a4e69fca1d1d73999b27
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633889"
---
# <a name="moderncomments_type-complextype-visio-xml"></a>ModernComments_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

||Valeur |
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
         <xs:complexType name="ModernComments_Type">
        <xs:sequence>
            <xs:element name="ModernCommentsList" type="ModernCommentsList_Type" minOccurs="0" maxOccurs="1" />
        </xs:sequence>
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ModernCommentsList](moderncommentslist-element-moderncomments_type-complextypevisio-xml.md) <br/> |[ModernCommentsList_Type](moderncommentslist_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés utilisées pour identifier le commentaire parent et les mentions présentes dans les commentaires d’un dessin.|
   
### <a name="attributes"></a>Attributs

Aucun.
