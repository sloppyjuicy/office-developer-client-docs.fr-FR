---
title: Élément PageSheet (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Spécifie les propriétés de la page de dessin associée à la page de dessin.
ms.openlocfilehash: 3b2d5e93e2b60133d6a5c8845625384aca79b792
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507724"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a>Élément PageSheet (Page_Type complexType) (Visio XML)

Spécifie les propriétés de la page de dessin associée à la page de dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une page dans le document. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme du remplissage. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin. |Valeurs du type xsd:unsignedInt. |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme des lignes. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin. |Valeurs du type xsd:unsignedInt. |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme du texte. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin. |Valeurs du type xsd:unsignedInt. |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:string. |
   

