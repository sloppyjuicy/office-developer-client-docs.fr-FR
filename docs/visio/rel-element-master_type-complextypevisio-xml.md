---
title: Élément Rel (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Spécifie une relation à un élément avec le XML maître correspondant.
ms.openlocfilehash: 3498f6560e6a4258ac3549af671d7233f7f17333
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772689"
---
# <a name="rel-element-master_type-complextype-visio-xml"></a>Élément Rel (Master_Type complexType) (Visio XML)

Spécifie une relation à un élément avec le XML maître correspondant.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Spécifie une instance de master XML stockée dans le dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Voir les remarques. |obligatoire  <br/> |Spécifie une relation à un élément. |« rId# »  <br/> Voir les remarques. |
   
## <a name="remarks"></a>Remarques

La valeur de **l’attribut r:id** doit **être ST_RelationshipID type** . Le **ST_RelationshipID** type est une chaîne qui doit être au format « rId# » où le caractère final doit être un nombre. Le nombre doit être unique parmi tous les éléments frères de **l’élément Rel** . 
  
Pour plus d’informations sur le type ST_RelationshipID, voir la spécification [ISO/IEC 29500 Partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

