---
title: Élément Rel (ForeignData_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Spécifie une relation entre une forme et une partie de document qui contient les données d’image associées à la forme.
ms.openlocfilehash: 1179468fc4679dc3aa6892949d0fe43fba55cb6d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623102"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a>Élément Rel (ForeignData_Type complexType) (Visio XML)

Spécifie une relation entre une forme et une partie de document qui contient les données d’image associées à la forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Spécifie une instance de données d’image stockées dans le dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Voir les remarques.  <br/> |obligatoire  <br/> |Spécifie une relation à un élément.  <br/> |« rId# »  <br/> Voir les remarques.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de **l’attribut r:id** doit être **ST_RelationshipID** type. Le ST_RelationshipID type est une chaîne qui doit être au format « rId# **»** où le caractère final doit être un nombre. Le nombre doit être unique parmi tous les éléments frères de **l’élément Rel.** 
  
Pour plus d’informations sur le type ST_RelationshipID, voir la spécification [ISO/IEC 29500 Partie 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)
  

