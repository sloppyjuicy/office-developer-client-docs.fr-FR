---
title: Élément RuleSet (RuleSets_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation du diagramme.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387390"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>Élément RuleSet (RuleSets_Type, complexType) (« Visio XML »)

Représente un ensemble de règles de validation du diagramme.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |validation.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Groupes de règles](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Inclut un élément **RuleSet** pour chaque règle de validation définie dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Règle](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés d’ensembles de règles.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Description  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation. Il s'agit par défaut d'une chaîne vide.  <br/> |Valeurs du type xsd : String.  <br/> |
|Activé  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si les règles de l’ensemble de règles de validation spécifié sont vérifiés lors de la validation est déclenchée pour le document actif. Valeur par défaut est True.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de l’ensemble de règles de validation.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom local de l’ensemble de règles de validation. La valeur par défaut à la valeur de l’attribut NameU.  <br/> |Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |obligatoire  <br/> |Spécifie le nom universel de l’ensemble de règles de validation.  <br/> |Valeurs du type xsd : String.  <br/> |
   

