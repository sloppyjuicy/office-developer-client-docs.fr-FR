---
title: Élément IssueTarget (Issue_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: En fonction de la cible de l’objet parent de validation, spécifie soit la page, ou la page et la forme, associé à ce problème de validation parent. Si la cible de la publication de validation parent est un document IssueTarget spécifie une page ni une forme.
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788896"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>Élément IssueTarget (Issue_Type, complexType) (« Visio XML »)

En fonction de la cible de l’objet parent de validation, spécifie soit la page, ou la page et la forme, associé à ce problème de validation parent. Si la cible de la publication de validation parent est un document **IssueTarget** spécifie une page ni une forme. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |validation.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
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
|PageID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la page qui est associée au problème de validation parent. Si la cible est le document, la valeur PageID peut être 0xFFFFFFFF.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’identificateur unique de la forme qui est associée au problème de validation parent. Si la cible est le document ou une page, la valeur ShapeID peut être 0xFFFFFFFF.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

