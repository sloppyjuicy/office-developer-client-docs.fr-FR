---
title: Rel, élément (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Spécifie une relation avec un composant avec les informations de liaison de données et de recordset associées.
ms.openlocfilehash: ca3584cfa8f1791e126d867a541de1fe9ec4b354
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360157"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a>Rel, élément (DataRecordSet_Type complexType) ('Visio XML')

Spécifie une relation avec un composant avec les informations de liaison de données et de recordset associées.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |pages. xml, Masters. xml, recordsets. xml, page #. xml, Master #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Spécifie une instance d'un jeu d'enregistrements et les informations de liaison de données stockées dans le dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|r:ID  <br/> |xsd: String  <br/> Voir les remarques.  <br/> |obligatoire  <br/> |Spécifie une relation avec un composant.  <br/> |«rId #»  <br/> Voir les remarques.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de l'attribut **r:ID** doit être un type **ST_RelationshipID** . Le type **ST_RelationshipID** est une chaîne qui doit être au format «rId #», où le dernier caractère doit être un nombre. Le nombre doit être unique parmi tous les éléments frères de l'élément **rel** . 
  
Pour plus d'informations sur le type ST_RelationshipID, reportez-vous à la [spécification ISO/IEC 29500 partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

