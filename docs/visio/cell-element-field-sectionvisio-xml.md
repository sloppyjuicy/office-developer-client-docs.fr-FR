---
title: Élément Cell (Section Champ) (Visio XML)
description: L’élément Cell (Section Champ) (Visio XML) affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
ms.openlocfilehash: 9f0c959b77eb3e9d33741a3447cd62062aa89bd9
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852532"
---
# <a name="cell-element-field-section-visio-xml"></a>Élément Cell (Section Champ) (Visio XML)

Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (section Field)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule prend la valeur d’une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de l’attribut **V** est la dernière valeur valide. |Chaîne de message d’erreur. |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée. |Formule. |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet. |Nom de la cellule ShapeSheet. Consultez la section Remarques ci-dessous. |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL. |Unités de la cellule. |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule. |Valeur de la cellule ShapeSheet. |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément **Cell** doit être l’un des ensembles limités de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** autorisées pour cet élément **Cell** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Calendrier  <br/> |Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date. |[Calendar, cellule (section Text Fields)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise. |[Format, cellule (section Text Fields)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indique le type de champ de texte. |[ObjectKind, cellule (section Text Fields)](objectkind-cell-text-fields-section.md) <br/> |
|Type  <br/> |Indique un type de données pour la valeur du champ de texte. |[Type, cellule (section Text Fields)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Détermine la catégorie d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue de format Champ et Données pour déterminer les informations de champ et de catégorie. |[UICategory, cellule (section Text Fields)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Détermine le code d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue de format Champ et Données pour déterminer les informations de champ et de catégorie. |[UICode, cellule (section Text Fields)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Détermine le format d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue format Champ et Données pour déterminer le champ et  <br/> |[UIFormat, cellule (section Text Fields)](uiformat-cell-text-fields-section.md) <br/> |
|Valeur  <br/> |Contient la fonction d'un champ. |[Value, cellule (section Text Fields)](value-cell-text-fields-section.md) <br/> |
   

