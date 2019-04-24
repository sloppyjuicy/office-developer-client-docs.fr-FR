---
title: Élément rule (RuleSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358799"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Élément rule (RuleSet_Type complexType) ('Visio XML')

Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |validation. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Représente un ensemble de règles de validation de diagramme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Spécifie l'expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Spécifie l'expression logique qui détermine si l'objet cible répond à la règle de validation.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Catégorie  <br/> |xsd: String  <br/> |facultatif  <br/> |Spécifie le texte affiché dans la colonne **catégorie** de la fenêtre problèmes. Il s'agit par défaut d'une chaîne vide.  <br/> |Valeurs du type xsd: String.  <br/> |
|Description  <br/> |xsd: String  <br/> |facultatif  <br/> |Spécifie la description de la règle de validation qui apparaît dans l'interface utilisateur. La valeur par défaut est «inconnu».  <br/> |Valeurs du type xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |Spécifie l'identificateur unique de la règle de validation.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Ignoré  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si la règle de validation est actuellement ignorée. La valeur par défaut est False.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|NameU  <br/> |xsd: String  <br/> |obligatoire  <br/> |Spécifie le nom universel de la règle de validation.  <br/> |Valeurs du type xsd: String.  <br/> |
|RuleTarget  <br/> |xsd: int  <br/> |facultatif  <br/> |Spécifie le type d'objet auquel la règle de validation s'applique.  <br/> |Valeurs du type xsd: int.  <br/> |
   

