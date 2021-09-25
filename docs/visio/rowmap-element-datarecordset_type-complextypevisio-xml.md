---
title: Élément RowMap (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Cartes ligne d’un recordset de données à une forme.
ms.openlocfilehash: 250829c1199e4936bbdef91fdf3ba61873ff54fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607779"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a>Élément RowMap (DataRecordSet_Type complexType) (Visio XML)

Cartes ligne d’un recordset de données à une forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

****

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de page de la forme liée aux données dans la ligne du data-recordset identifiée par **RowID**.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RowID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de ligne de la ligne, unique dans le recordset de données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de forme de la forme liée aux données dans la ligne du data-recordset identifiée par **RowID**.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

