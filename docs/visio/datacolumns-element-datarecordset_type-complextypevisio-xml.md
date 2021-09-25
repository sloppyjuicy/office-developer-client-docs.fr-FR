---
title: Élément DataColumns (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contient tous les éléments DataColumn d’un ensemble d’enregistrements de données.
ms.openlocfilehash: f850e6c4cb7e069c40f61e8efb63f932775d5ded
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582826"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a>Élément DataColumns (DataRecordSet_Type complexType) (Visio XML)

Contient tous les **éléments DataColumn** d’un ensemble d’enregistrements de données. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |Définit l’apparition d’une  colonne de données dans la fenêtre Données externes de l’interface utilisateur Visio et qualifie les données de la colonne en définissant son type de données et sa mise en forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Colonne sur laquelle trier les données.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|SortColumn  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique si la colonne **TriColumn** doit être trié par ordre croissant (1) ou décroit (0).  <br/> |Valeurs du type xsd:string.  <br/> |
   

