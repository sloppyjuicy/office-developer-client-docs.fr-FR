---
title: Élément RowMap (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Cartes ligne d’un recordset de données à une forme.
ms.openlocfilehash: a110575aa1bf3a70fae0ec764a41265acc670d2e
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521357"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a>Élément RowMap (DataRecordSet_Type complexType) (Visio XML)

Cartes ligne d’un recordset de données à une forme.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

****

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de page de la forme liée aux données dans la ligne du data-recordset identifiée par **RowID**. |Valeurs du type xsd:unsignedInt. |
|RowID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de ligne de la ligne, unique dans le recordset de données. |Valeurs du type xsd:unsignedInt. |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de forme de la forme liée aux données dans la ligne du data-recordset identifiée par **RowID**. |Valeurs du type xsd:unsignedInt. |
   

