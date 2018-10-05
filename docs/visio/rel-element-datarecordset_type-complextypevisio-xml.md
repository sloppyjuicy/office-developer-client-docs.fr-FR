---
title: Élément REL (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Spécifie une relation vers un composant avec le jeu d’enregistrements associée et les informations de liaison de données.
ms.openlocfilehash: ca3584cfa8f1791e126d867a541de1fe9ec4b354
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395314"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a>Élément REL (DataRecordSet_Type, complexType) (« Visio XML »)

Spécifie une relation vers un composant avec le jeu d’enregistrements associée et les informations de liaison de données.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |pages.XML, masters.xml, recordsets.xml, page # .xml, maître # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Spécifie une instance d’un jeu d’enregistrements et les informations de liaison de données stockées dans le dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|r : id  <br/> |XSD : String  <br/> Voir les remarques.  <br/> |obligatoire  <br/> |Spécifie une relation à un composant.  <br/> |« Supprimer # »  <br/> Voir les remarques.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de l’attribut **r : id** doit être un type **ST_RelationshipID** . Le type **ST_RelationshipID** est une chaîne qui doit être au format « débarrasser # », où le dernier caractère doit être un nombre. Le numéro doit être unique parmi tous les éléments frères de l’élément **Rel** . 
  
Pour plus d’informations sur le type ST_RelationshipID, consultez la [spécification ISO/IEC 29500 partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

