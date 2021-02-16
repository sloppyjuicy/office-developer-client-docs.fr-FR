---
title: Élément RuleFilter (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541679"
---
# <a name="rulefilter-element-rule_type-complextype-visio-xml"></a>Élément RuleFilter (Rule_Type complexType) (Visio XML)

Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Règle](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Formule  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la formule de l’élément.  <br/> |Valeurs de la chaîne xsd:string.  <br/> |
   

