---
title: Élément de cellule (Section de cellules définies par l’utilisateur) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ab7a11a0-a413-d4fe-ddf1-0d2e967dc21d
description: Une propriété d’un élément spécifié par l’utilisateur des informations susceptibles d’être référencées par d’autres cellules et outils de module complémentaire.
ms.openlocfilehash: 40555c58e6afdb3eefe5b1a14d4155ad4e57ed6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788221"
---
# <a name="cell-element-user-defined-cells-section-visio-xml"></a>Élément de cellule (Section de cellules définies par l’utilisateur) (« Visio XML »)

Une propriété d’un élément spécifié par l’utilisateur des informations susceptibles d’être référencées par d’autres cellules et outils de module complémentaire.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.XML, masters.xml, maître # .xml, pages.xml, page # .xml  <br/> |
   
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
|[Row, élément (Section de cellules définies par l’utilisateur)](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[UserRow_Type](userrow_type-complextypevisio-xml.md) <br/> |Une propriété d’un élément spécifié par l’utilisateur des informations susceptibles d’être référencées par d’autres cellules et outils de module complémentaire.  <br/> |
   
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
|Prompt  <br/> |Indique un message descriptif ou commentaire pour la cellule définie par l'utilisateur.  <br/> |[Prompt, cellule (section User-Defined Cells)](prompt-cell-user-defined-cells-section.md) <br/> |
|Valeur  <br/> |Indique une valeur pour la cellule définie par l'utilisateur correspondante.  <br/> |[Value, cellule (section User-Defined Cells)](value-cell-user-defined-cells-section.md) <br/> |
   

