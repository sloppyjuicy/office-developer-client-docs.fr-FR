---
title: PrimaryKey, élément (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifie une ou plusieurs colonnes de clé primaire du jeu d’enregistrements de données.
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789365"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a>PrimaryKey, élément (DataRecordSet_Type, complexType) (« Visio XML »)

Identifie une ou plusieurs colonnes de clé primaire du jeu d’enregistrements de données.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |recordsets.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[RowKeyValue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |Spécifie la valeur de ce composant de la clé primaire pour une ligne d’un objet recordset. Il doit exister au moins une occurrence de cet élément enfant.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnNameID  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom d’un champ qui est un composant de la clé primaire. Il doit être la valeur de l’attribut **ColumnNameID** d’un élément descendant DataColumn_Type de la DataRecordSet_Type dont la clé primaire est spécifiée.  <br/> |Valeurs du type xsd : String.  <br/> |
   

