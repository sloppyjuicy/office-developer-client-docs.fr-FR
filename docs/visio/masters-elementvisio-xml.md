---
title: Masters, élément (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contient la forme de base des éléments pour le document.
ms.openlocfilehash: ea2cee2f9845f8a72220081617a11cf4f72dafd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400991"
---
# <a name="masters-element-visio-xml"></a>Masters, élément (« Visio XML »)

Contient la forme de base des éléments pour le document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme de base](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent un masque du document.  <br/> |
|[MasterShortcut](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |Spécifie un raccourci de base défini dans le document.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

