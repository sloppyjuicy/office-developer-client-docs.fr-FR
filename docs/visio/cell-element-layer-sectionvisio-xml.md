---
title: Élément de cellule (Section Layer) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Spécifie une propriété d’un calque ou ses propriétés pour une page.
ms.openlocfilehash: e96fdc1dcd5c9a7a2cb8753beaff766c2b477af2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390974"
---
# <a name="cell-element-layer-section-visio-xml"></a>Élément de cellule (Section Layer) (« Visio XML »)

Spécifie une propriété d’un calque ou ses propriétés pour une page.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.XML, pages.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de ligne (section Calque)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’un calque ou ses propriétés pour une page.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD : String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur de **E** est la valeur actuelle (chaîne message d’erreur) ; la valeur de l’attribut de **V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |XSD : String  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir une des chaînes suivantes :  <br/>  « (une formule) » si la formule existe localement  <br/>  `No Formula`Si la formule est localement supprimée ou bloquée  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> |Représente le nom de la cellule de feuille ShapeSheet.  <br/> |Le nom de la cellule de feuille ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente une unité de mesure par défaut est la liste de distribution.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |La valeur de la cellule de feuille ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément de **cellule** doit être un ensemble limité de valeurs qui correspondent à des cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Actif  <br/> |Indique si un calque est actif.  <br/> |Aucune.  <br/> |
|Couleur  <br/> |Spécifie un des éléments suivants : l’index de la couleur de la table utilisée pour afficher le calque ou une valeur RVB spécifiant une couleur personnalisée pas dans la table des couleurs.  <br/> |Aucune.  <br/> |
|ColorTrans  <br/> |Détermine le degré de transparence d’un calque ou la couleur de texte de la forme, à partir de 0 (complètement opaque) et 1 (complètement transparent).  <br/> |Aucune.  <br/> |
|Collage  <br/> |Spécifie si les formes appartenant au calque peuvent être effectué un collage.  <br/> |Aucune.  <br/> |
|Lock  <br/> |Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.  <br/> |Aucune.  <br/> |
|Nom  <br/> |Le nom d’un calque.  <br/> |Aucune.  <br/> |
|NameUniv  <br/> |Indique le nom universel d’un calque.  <br/> |Aucune.  <br/> |
|Imprimer  <br/> |Spécifie si les formes appartenant au calque sont imprimés lorsque le dessin est imprimé.  <br/> |Aucune.  <br/> |
|Composant logiciel enfichable  <br/> |Spécifie si les autres formes peuvent s’aligner sur les formes attribuées au calque.  <br/> |Aucune.  <br/> |
|Status  <br/> |Indique si le calque est un calque valid pour un document.  <br/> |Aucune.  <br/> |
|Visible  <br/> |Indique si les formes appartenant au calque sont visibles sur la page de dessin.  <br/> |Aucun.  <br/> |
   

