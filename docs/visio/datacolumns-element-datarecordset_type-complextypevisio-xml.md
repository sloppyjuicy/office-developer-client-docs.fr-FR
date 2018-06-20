---
title: DataColumns, élément (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contient tous les éléments dans un jeu d’enregistrements de données DataColumn.
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788406"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a>DataColumns, élément (DataRecordSet_Type, complexType) (« Visio XML »)

Contient tous les éléments dans un jeu d’enregistrements de données **DataColumn** . 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |recordsets.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |Définit comment une colonne de données apparaît dans la fenêtre **Données externes** dans l’interface utilisateur Visio et qualifiant les données dans la colonne en définissant son type de données et de la mise en forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |La colonne sur lequel trier les données.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|SortColumn  <br/> |XSD : String  <br/> |facultatif  <br/> |Si le tri de la colonne **SortColumn** (1) par ordre croissant ou décroissant (0).  <br/> |Valeurs du type xsd : String.  <br/> |
   

