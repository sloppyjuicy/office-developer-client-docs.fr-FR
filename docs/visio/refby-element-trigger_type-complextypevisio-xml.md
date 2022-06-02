---
title: Élément RefBy (Trigger_Type complexType) (Visio XML)
description: Décrit la description et les informations d’élément parent/enfant pour l’élément RefBy (Trigger_Type complexType), qui spécifie une référence à une page dans le dessin.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
ms.openlocfilehash: 75c6186c1a516762432d35a412040281ac2ca447
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852515"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a>Élément RefBy (Trigger_Type complexType) (Visio XML)

Spécifie une référence à une page dans le dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> ||
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Fournit des instructions à Microsoft Visio pour recalculer une relation entre les parties de document dans un fichier Visio. |

   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’attribut ID d’une page dans le dessin. |Valeurs du type xsd:unsignedInt. |
|T  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le type de référence. |Valeurs du type xsd:string. |
   

