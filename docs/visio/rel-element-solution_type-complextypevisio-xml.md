---
title: Élément REL (Solution_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Spécifie une relation vers un composant de la solution que XML associé à cette solution.
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789419"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a>Élément REL (Solution_Type, complexType) (« Visio XML »)

Spécifie une relation vers un composant de la solution que XML associé à cette solution.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |pages.XML, masters.xml, recordsets.xml, page # .xml, maître # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Probl?me](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |Spécifie une instance d’une solution que XML stocké dans le dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|r : id  <br/> |XSD : String  <br/> Voir les remarques.  <br/> |obligatoire  <br/> |Spécifie une relation à un composant.  <br/> |« Supprimer # »  <br/> Voir les remarques.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de l’attribut **r : id** doit être un type **ST_RelationshipID** . Le type **ST_RelationshipID** est une chaîne qui doit être au format « débarrasser # », où le dernier caractère doit être un nombre. Le numéro doit être unique parmi tous les éléments frères de l’élément **Rel** . 
  
Pour plus d’informations sur le type ST_RelationshipID, consultez la [spécification ISO/IEC 29500 partie 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

