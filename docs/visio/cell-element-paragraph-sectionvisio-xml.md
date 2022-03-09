---
title: Élément de cellule (section Paragraph) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Spécifie un attribut de mise en forme de paragraphe pour le texte de la forme, tel que les retraits, l’espacement des lignes, les puces ou l’alignement horizontal des paragraphes.
ms.openlocfilehash: 735b2f986bfe59d99ed7f365433cb69f122be1d9
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404656"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Élément de cellule (section Paragraph) (Visio XML)

Spécifie un attribut de mise en forme de paragraphe pour le texte de la forme, tel que les retraits, l’espacement des lignes, les puces ou l’alignement horizontal des paragraphes.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
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
|[Élément Row (section Paragraph)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme de paragraphe pour le texte de la forme, tel que les retraits, l’espacement des lignes, les puces ou l’alignement horizontal des paragraphes. |
   
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
|Bullet  <br/> |Détermine le style de puce. |[Bullet, cellule (section Paragraph)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Représente le numéro de la police utilisée pour mettre en forme le texte lorsqu'une chaîne de puces personnalisée est spécifiée et que la valeur dans la cellule Bullet est non nulle. |[BulletFont, cellule (section Paragraph)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |Indique la taille d'une puce. |[BulletSize, cellule (section Paragraph)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |Permet de créer un style de puce personnalisé. |[BulletString, cellule (section Paragraph)](bulletstring-cell-paragraph-section.md) <br/> |
|Flags  <br/> |Indique si l'orientation du texte est de gauche à droite ou de droite à gauche. |[Flags, cellule (section Paragraph)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |Détermine l'alignement horizontal du texte dans le bloc de texte de la forme. |[HAlign, cellule (section Paragraph)](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |Représente la distance entre la première ligne de chaque paragraphe du bloc de texte et le retrait gauche du paragraphe. Cette valeur est indépendante de l'échelle de dessin. Elle ne change pas si le dessin est mis à l'échelle. |[IndFirst, cellule (section Paragraph)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle. |[IndLeft, cellule (section Paragraph)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Représente la distance entre chaque ligne du paragraphe et la marge droite du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle. |[IndRight, cellule (section Paragraph)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin. |[SpAfter, cellule (section Paragraph)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin. |[SpBefore, cellule (section Paragraph)](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte. |[SpLine, cellule (section Paragraph)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Représente la distance entre la première ligne du paragraphe et la puce. |[TextPosAfterBullet, cellule (section Paragraph)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

