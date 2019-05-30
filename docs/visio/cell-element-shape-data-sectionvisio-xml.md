---
title: Élément de cellule (section données de forme) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Spécifie une propriété des données de forme.
ms.openlocfilehash: 3a6238f19f27d001d3c9eebcbcec720822a0ed40
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539375"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Élément de cellule (section données de forme) (XML Visio)

Spécifie une propriété des données de forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Master #. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de ligne (section données de forme)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Forme type_de_données](propertyrow_type-complextypevisio-xml.md) <br/> |Spécifie une entrée de données de forme pour l’Association de données à une forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur **E** est la valeur actuelle (chaîne de message d’erreur); la valeur de l’attribut **V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |xsd: String  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes:  <br/>  ' (une formule) 'si la formule existe localement  <br/>  `No Formula`Si la formule est supprimée ou bloquée localement  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Consultez la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente une unité de mesure la valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément de **cellule** doit correspondre à l’un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Calendrier  <br/> |Indique le type de calendrier utilisé lorsque le Type d'un élément de données de forme est Date.  <br/> |[Calendar, cellule (section Custom Properties)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Indique si la ligne de données de forme est liée à un champ dans un jeu d’enregistrements de données.  <br/> ||
|Format  <br/> |Définit la mise en forme d'un élément de données de forme qui est une chaîne, une liste fixe, un nombre, une liste variable, une date, une heure ou une monnaie.  <br/> |[Format, cellule (section Shape Data)](format-cell-shape-data-section.md) <br/> |
|Visibilité  <br/> |Détermine si l’élément de données de forme est visible ou non dans la fenêtre Données de forme.  <br/> |[Invisible, cellule (section Shape Data)](invisible-cell-shape-data-section.md) <br/> |
|Étiquette  <br/> |Indique l’intitulé que les utilisateurs voient s’afficher dans la fenêtre  Données de forme. Un intitulé se compose de caractères alphanumériques dont le caractère de soulignement (_).  <br/> |[Label, cellule (section Shape Data)](label-cell-shape-data-section.md) <br/> |
|ID  <br/> |Indique la langue dans laquelle les données forme ont été entrées.  <br/> |[LangID, cellule (section Shape Data)](langid-cell-shape-data-section.md) <br/> |
|Invite  <br/> |Contient la description ou l’instruction qui apparaît sous la forme d’un conseil lorsque vous positionnez la souris sur la valeur dans la fenêtre Données de forme.  <br/> |[Prompt, cellule (section Shape Data)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Produit une chaîne qui détermine l’ordre dans lequel les éléments de la fenêtre Données de forme sont présentés.  <br/> |[SortKey, cellule (section Shape Data)](sortkey-cell-shape-data-section.md) <br/> |
|Type  <br/> |Indique le type des données de forme.  <br/> |[Type, cellule (section Shape Data)](type-cell-shape-data-section.md) <br/> |
|Valeur  <br/> |Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue Définir les données de forme.  <br/> |[Value, cellule (section Shape Data)](value-cell-shape-data-section.md) <br/> |
|Vérifié  <br/> |Indique si l’utilisateur est invité à entrer des informations de propriétés personnalisées pour une forme lorsqu’une instance est créée ou lorsque la forme est dupliquée ou copiée.  <br/> |Aucun.  <br/> |
   

