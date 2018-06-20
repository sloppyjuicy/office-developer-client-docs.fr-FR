---
title: Élément RuleInfo (Issue_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Spécifie des informations sur la règle de validation concerne le problème de validation parent.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789560"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>Élément RuleInfo (Issue_Type, complexType) (« Visio XML »)

Spécifie des informations sur la règle de validation concerne le problème de validation parent.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |validation.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Problème](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Représente un problème de validation unique dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID de la règle  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la règle de validation concerne le problème parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RuleSetID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de l’ensemble de règles de validation concerne le problème parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

