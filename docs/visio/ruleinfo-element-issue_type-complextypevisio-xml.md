---
title: Élément RuleInfo (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Spécifie les informations relatives à la règle de validation à qui appartient le problème de validation parent.
ms.openlocfilehash: 367c678d14531bd9e9d5dc86956aeb0ff42757fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623018"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a>Élément RuleInfo (Issue_Type complexType) (Visio XML)

Spécifie les informations relatives à la règle de validation à qui appartient le problème de validation parent.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Problème](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Représente un problème de validation unique dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la règle de validation à qui appartient le problème parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RuleSetID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de l’ensemble de règles de validation à qui appartient le problème parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

