---
title: Élément de cellule (section Layer) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Spécifie une propriété pour un calque ou ses propriétés pour une page.
ms.openlocfilehash: 5de2289441ac6be71fe8dc332b4900d5523475dd
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406322"
---
# <a name="cell-element-layer-section-visio-xml"></a>Élément de cellule (section Layer) (Visio XML)

Spécifie une propriété pour un calque ou ses propriétés pour une page.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |masters.xml, pages.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Layer Section)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Spécifie une propriété pour un calque ou ses propriétés pour une page. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide. |Chaîne de message d’erreur. |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée. |Formule. |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet. |Nom de la cellule ShapeSheet. Voir la section Remarques ci-dessous. |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL. |Unités de la cellule. |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule. |Valeur de la cellule ShapeSheet. |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit être l’un des ensembles limités de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Actif  <br/> |Spécifie si un calque est actif. |Aucun. |
|Couleur  <br/> |Spécifie l’une des valeurs suivantes : l’index de la couleur dans le tableau de couleurs utilisé pour afficher le calque ou une valeur RVB spécifiant une couleur personnalisée qui n’est pas dans le tableau de couleurs. |Aucun. |
|ColorTrans  <br/> |Détermine le degré de transparence de la couleur du texte d’un calque ou d’une forme, de 0 (complètement opaque) à 1 (complètement transparent). |Aucun. |
|Glue  <br/> |Spécifie si les formes appartenant au calque peuvent être collées. |Aucun. |
|Lock  <br/> |Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification. |Aucun. |
|Nom  <br/> |Nom d’un calque. |Aucun. |
|NameUniv  <br/> |Spécifie le nom universel d’un calque. |Aucun. |
|Imprimer  <br/> |Spécifie si les formes appartenant au calque sont imprimées lors de l’impression du dessin. |Aucun. |
|Aligner  <br/> |Spécifie si d’autres formes peuvent s’aligner sur les formes affectées au calque. |Aucun. |
|Statut  <br/> |Spécifie si le calque est un calque valide pour un document. |Aucun. |
|Visible  <br/> |Indique si les formes appartenant au calque sont visibles sur la page de dessin. |Aucun. |
   

