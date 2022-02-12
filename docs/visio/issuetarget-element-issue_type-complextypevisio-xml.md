---
title: Élément IssueTarget (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Selon la cible du problème de validation parent, spécifie la page, ou la page et la forme, associées au problème de validation parent. Si la cible du problème de validation parent est un document, IssueTarget ne spécule ni une page, ni une forme.
ms.openlocfilehash: dea4fa9af82798447d70e2c4060d220821f22164
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775545"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a>Élément IssueTarget (Issue_Type complexType) (Visio XML)

Selon la cible du problème de validation parent, spécifie la page, ou la page et la forme, associées au problème de validation parent. Si la cible du problème de validation parent est un document, **IssueTarget** ne spécule ni une page, ni une forme. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Problème](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Représente un problème de validation unique dans le document. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la page associée au problème de validation parent. Si la cible est le document, la valeur PageID peut être 0xFFFFFFFF. |Valeurs du type xsd:unsignedInt. |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la forme associée au problème de validation parent. Si la cible est le document ou une page, la valeur ShapeID peut être 0xFFFFFFFF. |Valeurs du type xsd:unsignedInt. |
   

