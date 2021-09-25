---
title: Élément RefBy (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Spécifie une référence à une page du dessin.
ms.openlocfilehash: 4b38c508b2c6d417ffbddbf1cfed9945050ce670
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565904"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a>Élément RefBy (Trigger_Type complexType) (Visio XML)

Spécifie une référence à une page du dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> ||
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Fournit des instructions à Microsoft Visio pour recalculer une relation entre les composants de document dans Visio fichier.  <br/> |

   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’attribut ID d’une page dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|T  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le type de référence.  <br/> |Valeurs du type xsd:string.  <br/> |
   

