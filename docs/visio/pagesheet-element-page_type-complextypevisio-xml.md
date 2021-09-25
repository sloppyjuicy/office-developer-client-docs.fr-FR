---
title: Élément PageSheet (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Spécifie les propriétés de la page de dessin associée à la page de dessin.
ms.openlocfilehash: 26ab066a8539a1c464afb3eebedf59c2f1a54afa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554235"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a>Élément PageSheet (Page_Type complexType) (Visio XML)

Spécifie les propriétés de la page de dessin associée à la page de dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une page dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme du remplissage. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme des lignes. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme du texte. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd:string.  <br/> |
   

