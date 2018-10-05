---
title: Élément REL (ForeignData_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Spécifie une relation entre une forme et un composant de document qui contient les données d’image associées à la forme.
ms.openlocfilehash: 2667d5b0b940384f10df62dfc0fbf6acfa7d4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383442"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a>Élément REL (ForeignData_Type, complexType) (« Visio XML »)

Spécifie une relation entre une forme et un composant de document qui contient les données d’image associées à la forme.
  
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
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Spécifie une seule instance de données d’image stockées dans le dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|r : id  <br/> |XSD : String  <br/> Voir les remarques.  <br/> |obligatoire  <br/> |Spécifie une relation à un composant.  <br/> |« Supprimer # »  <br/> Voir les remarques.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de l’attribut **r : id** doit être un type **ST_RelationshipID** . Le type **ST_RelationshipID** est une chaîne qui doit être au format « débarrasser # », où le dernier caractère doit être un nombre. Le numéro doit être unique parmi tous les éléments frères de l’élément **Rel** . 
  
Pour plus d’informations sur le type ST_RelationshipID, consultez la [spécification ISO/IEC 29500 partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

