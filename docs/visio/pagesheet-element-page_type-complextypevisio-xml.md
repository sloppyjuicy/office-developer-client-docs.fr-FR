---
title: Élément PageSheet (Page_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Cette énumération spécifie les propriétés de la page de dessin associée à la page de dessin.
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326116"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>Élément PageSheet (Page_Type complexType) ('Visio XML')

Cette énumération spécifie les propriétés de la page de dessin associée à la page de dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |pages. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent une page dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l'ID de la feuille de style à partir de laquelle hériter la mise en forme du remplissage. Il doit s'agir de la valeur de l'attribut **ID** associé à un **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|LineStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l'ID de la feuille de style à partir de laquelle hériter la mise en forme des lignes. Il doit s'agir de la valeur de l'attribut **ID** associé à un **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|TextStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l'ID de la feuille de style à partir de laquelle hériter la mise en forme du texte. Il doit s'agir de la valeur de l'attribut **ID** associé à un **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |facultatif  <br/> |ID unique de l'élément au sein de son élément parent.  <br/> |Valeurs du type xsd: String.  <br/> |
   

