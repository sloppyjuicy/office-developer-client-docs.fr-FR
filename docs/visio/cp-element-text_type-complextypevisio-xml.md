---
title: élément cp (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marque le début d’une exécute de propriétés de caractères mise en forme en fonction de l’élément Char correspondant. La suite est définie à la fin du texte ou jusqu’à la balise suivante.
ms.openlocfilehash: 1dde00dc4a3f85d0bfc7389f0797dfce33acb444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586634"
---
# <a name="cp-element-text_type-complextype-visio-xml"></a>élément cp (Text_Type complexType) (Visio XML)

Marque le début d’une exécute de propriétés de caractères mise en forme en fonction de l’élément Char correspondant. La suite est définie à la fin du texte ou jusqu’à la balise suivante.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contient le texte d’une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Index de l’élément Char que cette propriété run représente.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

