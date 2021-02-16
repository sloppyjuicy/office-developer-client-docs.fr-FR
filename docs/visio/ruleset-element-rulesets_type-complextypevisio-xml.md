---
title: Élément RuleSet (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation de diagramme.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541637"
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Inclut **un élément RuleSet** pour chaque ensemble de règles de validation dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Règle](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’ensemble de règles.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Description  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation. Il s'agit par défaut d'une chaîne vide.  <br/> |Valeurs du type xsd:string.  <br/> |
|Activé  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si les règles de l’ensemble de règles de validation spécifié sont vérifiées lorsque la validation est déclenchée pour le document actuel. La valeur par défaut est True.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de l’ensemble de règles de validation.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom local de l’ensemble de règles de validation. Valeur par défaut de l’attribut NameU.  <br/> |Valeurs du type xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le nom universel de l’ensemble de règles de validation.  <br/> |Valeurs du type xsd:string.  <br/> |
   

