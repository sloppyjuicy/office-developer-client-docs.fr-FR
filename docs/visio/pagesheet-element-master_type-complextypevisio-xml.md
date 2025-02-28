---
title: Élément PageSheet (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Spécifie les propriétés de la page de dessin associée à la page de dessin.
ms.openlocfilehash: 6f5e89bada95d35b956d4702e92e65c92e8b0016
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626219"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a>Élément PageSheet (Master_Type complexType) (Visio XML)

Spécifie les propriétés de la page de dessin associée à la page de dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |masters.xml  <br/> |
   
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
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Spécifie une master dans un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme du remplissage. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin. |Valeurs du type xsd:unsignedInt. |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme des lignes. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin. |Valeurs du type xsd:unsignedInt. |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir de laquelle hériter la mise en forme du texte. Il DOIT s’agit de la valeur de **l’attribut ID** associé à un **StyleSheet_Type** dans le dessin. |Valeurs du type xsd:unsignedInt. |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:string. |
   

