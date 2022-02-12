---
title: Élément Rule (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.
ms.openlocfilehash: f3892aa517613687eb01026123b40bb7e24fcef9
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779396"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a>Élément Rule (RuleSet_Type complexType) (Visio XML)

Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Représente un ensemble de règles de validation de diagramme. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible. |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Spécifie l’expression logique qui détermine si l’objet cible satisfait à la règle de validation. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Catégorie  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le texte affiché dans la colonne **Catégorie** de la fenêtre Problèmes. Il s'agit par défaut d'une chaîne vide. |Valeurs du type xsd:string. |
|Description  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie la description de la règle de validation qui apparaît dans l’interface utilisateur. La valeur par défaut est « Unknown ». |Valeurs du type xsd:string. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la règle de validation. |Valeurs du type xsd:unsignedInt. |
|Ignoré  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si la règle de validation est actuellement ignorée. La valeur par défaut est False. |Valeurs du type xsd:boolean. |
|NameU  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le nom universel de la règle de validation. |Valeurs du type xsd:string. |
|RuleTarget  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie le type d’objet auquel la règle de validation s’applique. |Valeurs du type xsd:int. |
   

