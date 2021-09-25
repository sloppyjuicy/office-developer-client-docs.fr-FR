---
title: Élément de cellule (section Field) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
ms.openlocfilehash: fffa97458b083edc7df33c4a559fa987f2bb1bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594894"
---
# <a name="cell-element-field-section-visio-xml"></a>Élément de cellule (section Field) (Visio XML)

Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Field Section)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée.  <br/> |Formule.  <br/> |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit faire partie d’un ensemble limité de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell.** 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Calendrier  <br/> |Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.  <br/> |[Calendar, cellule (section Text Fields)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.  <br/> |[Format, cellule (section Text Fields)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indique le type de champ de texte.  <br/> |[ObjectKind, cellule (section Text Fields)](objectkind-cell-text-fields-section.md) <br/> |
|Type  <br/> |Indique un type de données pour la valeur du champ de texte.  <br/> |[Type, cellule (section Text Fields)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Détermine la catégorie d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue Champ et Format de données pour déterminer les informations de champ et de catégorie.  <br/> |[UICategory, cellule (section Text Fields)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Détermine le code d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue Champ et Format de données pour déterminer les informations de champ et de catégorie.  <br/> |[UICode, cellule (section Text Fields)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Détermine le format d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue Champ et Format de données pour déterminer le champ et  <br/> |[UIFormat, cellule (section Text Fields)](uiformat-cell-text-fields-section.md) <br/> |
|Valeur  <br/> |Contient la fonction d'un champ.  <br/> |[Value, cellule (section Text Fields)](value-cell-text-fields-section.md) <br/> |
   

