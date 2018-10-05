---
title: élément TP (Text_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Spécifie le début d’un propriétés onglets exécuter. L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.
ms.openlocfilehash: 3f27ea0babefa0ea69cbbc361031c57602649107
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397547"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a>élément TP (Text_Type, complexType) (« Visio XML »)

Spécifie le début d’un propriétés onglets exécuter. L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[tp_Type](tp_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |page # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contient le texte d’une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Index de base zéro de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

