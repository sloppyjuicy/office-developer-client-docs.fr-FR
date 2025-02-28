---
title: Élément de cellule (section Shape Data) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Spécifie une propriété des données de forme.
ms.openlocfilehash: c832875f7d49db57520087b7432230d18d0dc73d
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406471"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Élément de cellule (section Shape Data) (Visio XML)

Spécifie une propriété des données de forme.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Row, élément (shape data section)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Forme Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Spécifie une entrée de données de forme pour l’association de données à une forme. |
   
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
|Calendrier  <br/> |Indique le type de calendrier utilisé lorsque le Type d'un élément de données de forme est Date. |[Calendar, cellule (section Custom Properties)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Indique si la ligne Données de forme est actuellement liée à un champ dans un jeu d’enregistrements de données. ||
|Format  <br/> |Définit la mise en forme d'un élément de données de forme qui est une chaîne, une liste fixe, un nombre, une liste variable, une date, une heure ou une monnaie. |[Format, cellule (section Shape Data)](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Détermine si l’élément de données de forme est visible ou non dans la fenêtre Données de forme. |[Invisible, cellule (section Shape Data)](invisible-cell-shape-data-section.md) <br/> |
|Étiquette  <br/> |Indique l’intitulé que les utilisateurs voient s’afficher dans la fenêtre  Données de forme. Un intitulé se compose de caractères alphanumériques dont le caractère de soulignement (_). |[Label, cellule (section Shape Data)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Indique la langue dans laquelle les données forme ont été entrées. |[LangID, cellule (section Shape Data)](langid-cell-shape-data-section.md) <br/> |
|Invite  <br/> |Contient la description ou l’instruction qui apparaît sous la forme d’un conseil lorsque vous positionnez la souris sur la valeur dans la fenêtre Données de forme. |[Prompt, cellule (section Shape Data)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Produit une chaîne qui détermine l’ordre dans lequel les éléments de la fenêtre Données de forme sont présentés. |[SortKey, cellule (section Shape Data)](sortkey-cell-shape-data-section.md) <br/> |
|Type  <br/> |Indique le type des données de forme. |[Type, cellule (section Shape Data)](type-cell-shape-data-section.md) <br/> |
|Valeur  <br/> |Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue Définir les données de forme. |[Value, cellule (section Shape Data)](value-cell-shape-data-section.md) <br/> |
|Vérifier  <br/> |Spécifie si l’utilisateur est interrogé pour entrer des informations sur les propriétés personnalisées d’une forme lors de la création d’une instance ou de la duplication ou de la copie de la forme. |Aucun. |
   

