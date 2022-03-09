---
title: ModernCommentEntry_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: 3544287fb00c6487eda22773aad60b34d1772799
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371628"
---
# <a name="moderncommententry_type-complextype-visio-xml"></a>ModernCommentEntry_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
 <xs:complexType name="ModernCommentEntry_Type">
        <xs:sequence>
            <xs:element name="MentionsList" type="MentionsList_Type" minOccurs="0" maxOccurs="1" />
            <xs:any minOccurs="0" maxOccurs="unbounded" namespace="##any" processContents="lax" />
        </xs:sequence>
        <xs:attribute name="CommentID" type="xs:unsignedInt" use="required" />
        <xs:attribute name="ParentID" type="xs:unsignedInt" />
        <xs:anyAttribute namespace="##other" processContents="lax" />
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[MentionsList](mentionslist-element-moderncommententry_type-complextypevisio-xml.md) <br/> |[MentionsList_Type](mentionslist_type-complextypevisio-xml.md) <br/> ||
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CommentID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|ParentID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
   

