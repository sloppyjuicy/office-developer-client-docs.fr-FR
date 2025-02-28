---
title: MentionEntry_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: 9c8954ab910312c96e144f79246f234203b4ac48
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426376"
---
# <a name="mentionentry_type-complextype-visio-xml"></a>MentionEntry_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

||Valeur |
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
        <xs:complexType name="MentionEntry_Type">
        <xs:sequence>
            <xs:any minOccurs="0" maxOccurs="unbounded" namespace="##any" processContents="lax" />
        </xs:sequence>
        <xs:attribute name="MentionCheckSum" type="xs:unsignedInt" use="required" />
        <xs:attribute name="MentionPersonID" type="xs:unsignedInt" use="required" />
        <xs:attribute name="MentionID" type="xs:unsignedInt" use="required" />
        <xs:attribute name="StartIndex" type="xs:unsignedInt" use="required" />
        <xs:attribute name="Length" type="xs:unsignedInt" use="required" />
        <xs:anyAttribute namespace="##other" processContents="lax" />
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|MentionCheckSum  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|MentionPersonID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|MentionID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|StartIndex  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|Longueur  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
   

