---
title: Élément RuleInfo (complexType Issue_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356986"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>Élément RuleInfo (complexType Issue_Type) ('Visio XML')

Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |validation. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Problème](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Représente un problème de validation unique dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |Spécifie l'identificateur unique de la règle de validation à laquelle le problème parent est lié.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|RuleSetID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |Spécifie l'identificateur unique de l'ensemble de règles de validation auquel le problème parent se rapporte.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

