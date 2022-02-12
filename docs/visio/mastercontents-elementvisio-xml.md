---
title: Élément MasterContents (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Spécifie des informations sur les formes d’une forme de base dans un dessin.
ms.openlocfilehash: fa622c3fcccd91a29cef7ed4af90f4c42fc7d6a2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788863"
---
# <a name="mastercontents-element-visio-xml"></a>Élément MasterContents (Visio XML)

Spécifie des informations sur les formes d’une forme de base dans un dessin. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin. |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Contient une collection **d’éléments Shape** . |
   
### <a name="attributes"></a>Attributs

Aucun.
  

