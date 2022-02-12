---
title: Élément RowKeyValue (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Spécifie la valeur d’une clé primaire pour une ligne individuelle d’un recordset.
ms.openlocfilehash: 36938e7a1d348bd4c00778b2a58776d2f9b2e62c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772640"
---
# <a name="rowkeyvalue-element-primarykey_type-complextype-visio-xml"></a>Élément RowKeyValue (PrimaryKey_Type complexType) (Visio XML)

Spécifie la valeur d’une clé primaire pour une ligne individuelle d’un recordset.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Spécifie une clé primaire d’un recordset. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|RowID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Valeur unique qui identifie une ligne d’un recordset. |Valeurs du type xsd:unsignedInt. |
|Valeur  <br/> |xsd:string  <br/> |obligatoire  <br/> |Valeur de la clé primaire pour cette ligne du recordset. |Valeurs du type xsd:string. |
   

