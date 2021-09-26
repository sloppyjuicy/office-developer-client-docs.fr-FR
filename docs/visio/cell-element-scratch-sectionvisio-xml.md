---
title: Élément de cellule (section Scratch) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: af17b1c5-51ee-f46f-79d0-4f33369b66f1
description: Spécifie une zone de travail pour l’entrée et le test de formules qui peuvent être référentes par d’autres cellules.
ms.openlocfilehash: f856195c9fb697ac265f23a0348a83c47b4987ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613092"
---
# <a name="cell-element-scratch-section-visio-xml"></a>Élément de cellule (section Scratch) (Visio XML)

Spécifie une zone de travail pour l’entrée et le test de formules qui peuvent être référentes par d’autres cellules.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (section Scratch)](row-element-scratch-sectionvisio-xml.md) <br/> |[ScratchRow_Type](scratch_type-complextypevisio-xml.md) <br/> |Spécifie une zone de travail pour l’entrée et le test de formules qui peuvent être référentes par d’autres cellules.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée.  <br/> |Formule.  <br/> |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
### <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit faire partie d’un ensemble limité de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell.** 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|A  <br/> |Cellule de montage utilisable pour entrer ou tester des formules.  <br/> |[Scratch, section](scratch-section.md) <br/> |
|B  <br/> |Cellule de montage utilisable pour entrer ou tester des formules.  <br/> |[Scratch, section](scratch-section.md) <br/> |
|C  <br/> |Cellule de montage utilisable pour entrer ou tester des formules.  <br/> |[Scratch, section](scratch-section.md) <br/> |
|D  <br/> |Cellule de montage utilisable pour entrer ou tester des formules.  <br/> |[Scratch, section](scratch-section.md) <br/> |
|X  <br/> |Cellule de montage utilisable pour entrer ou tester des formules.  <br/> |[Scratch, section](scratch-section.md) <br/> |
|O  <br/> |Cellule de montage utilisable pour entrer ou tester des formules.  <br/> |[Scratch, section](scratch-section.md) <br/> |
   

