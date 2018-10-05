---
title: Élément de cellule (Section champ) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
ms.openlocfilehash: f6c3c724b210ad579012ff58b93333e28c2a8cf1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383337"
---
# <a name="cell-element-field-section-visio-xml"></a>Élément de cellule (Section champ) (« Visio XML »)

Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master # .xml, page # .xml  <br/> |
   
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
|[Élément de ligne (section Champ)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.  <br/> |
   
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
|Calendrier  <br/> |Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.  <br/> |[Calendar, cellule (section Text Fields)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.  <br/> |[Format, cellule (section Text Fields)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indique le type de champ de texte.  <br/> |[ObjectKind, cellule (section Text Fields)](objectkind-cell-text-fields-section.md) <br/> |
|Type  <br/> |Indique un type de données pour la valeur du champ de texte.  <br/> |[Type, cellule (section Text Fields)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Détermine la catégorie d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue format de champ et les données pour déterminer les informations de champ et de catégorie.  <br/> |[UICategory, cellule (section Text Fields)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Détermine le code d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue format de champ et les données pour déterminer les informations de champ et de catégorie.  <br/> |[UICode, cellule (section Text Fields)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Détermine le format d’un champ inséré. Cette cellule est utilisée par les boîtes de dialogue format de champ et les données pour déterminer le champ et  <br/> |[UIFormat, cellule (section Text Fields)](uiformat-cell-text-fields-section.md) <br/> |
|Valeur  <br/> |Contient la fonction d'un champ.  <br/> |[Value, cellule (section Text Fields)](value-cell-text-fields-section.md) <br/> |
   

