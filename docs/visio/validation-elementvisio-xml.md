---
title: Validation, élément ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Stocke les informations relatives à la validation du diagramme pour le document.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329082"
---
# <a name="validation-element-visio-xml"></a>Validation, élément ('Visio XML')

Stocke les informations relatives à la validation du diagramme pour le document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |validation. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Issues](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |Contient tous les éléments de **problème** pour le document.  <br/> |
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Inclut un élément **RuleSet** pour chaque ensemble de règles de validation dans le document.  <br/> |
|[ValidationProperties](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |EnCapsule les propriétés liées à la validation du document.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

