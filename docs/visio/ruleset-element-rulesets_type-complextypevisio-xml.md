---
title: Élément RuleSet (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation de diagramme.
ms.openlocfilehash: 0bc8dca91699b0fcf94582a82306feaf5c716ea4
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781946"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a>Élément RuleSet (RuleSets_Type complexType) (Visio XML)

Représente un ensemble de règles de validation de diagramme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Inclut **un élément RuleSet** pour chaque ensemble de règles de validation dans le document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Règle](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Représente une règle de validation unique dans un ensemble de règles de validation de diagramme. |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’ensemble de règles. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Description  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation. Il s'agit par défaut d'une chaîne vide. |Valeurs du type xsd:string. |
|Activé  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si les règles de l’ensemble de règles de validation spécifié sont vérifiées lorsque la validation est déclenchée pour le document actuel. La valeur par défaut est True. |Valeurs du type xsd:boolean. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de l’ensemble de règles de validation. |Valeurs du type xsd:unsignedInt. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom local de l’ensemble de règles de validation. Valeur par défaut de l’attribut NameU. |Valeurs du type xsd:string. |
|NameU  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le nom universel de l’ensemble de règles de validation. |Valeurs du type xsd:string. |
   

