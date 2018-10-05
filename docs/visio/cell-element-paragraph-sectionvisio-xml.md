---
title: Élément de cellule (Section paragraphe) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Spécifie un attribut pour le texte de la forme, telles que les retraits, l’espacement des lignes, des puces ou alignement horizontal des paragraphes de la mise en forme de paragraphe.
ms.openlocfilehash: 2647ce92b38234e4d6fc4d6bc59188d468332ca8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383471"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Élément de cellule (Section paragraphe) (« Visio XML »)

Spécifie un attribut pour le texte de la forme, telles que les retraits, l’espacement des lignes, des puces ou alignement horizontal des paragraphes de la mise en forme de paragraphe.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.XML, master # .xml, page # .xml  <br/> |
   
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
|[Élément de ligne (section Paragraphe)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Spécifie un attribut pour le texte de la forme, telles que les retraits, l’espacement des lignes, des puces ou alignement horizontal des paragraphes de la mise en forme de paragraphe.  <br/> |
   
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
|Puce  <br/> |Détermine le style de puce.  <br/> |[Bullet, cellule (section Paragraph)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Représente le numéro de la police utilisée pour mettre en forme le texte lorsqu'une chaîne de puces personnalisée est spécifiée et que la valeur dans la cellule Bullet est non nulle.  <br/> |[BulletFont, cellule (section Paragraph)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |Indique la taille d'une puce.  <br/> |[BulletSize, cellule (section Paragraph)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |Permet de créer un style de puce personnalisé.  <br/> |[BulletString, cellule (section Paragraph)](bulletstring-cell-paragraph-section.md) <br/> |
|Indicateurs  <br/> |Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.  <br/> |[Flags, cellule (section Paragraph)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.  <br/> |[HAlign, cellule (section Paragraph)](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |Représente la distance entre la première ligne de chaque paragraphe du bloc de texte et le retrait gauche du paragraphe. Cette valeur est indépendante de l'échelle de dessin. Elle ne change pas si le dessin est mis à l'échelle.  <br/> |[IndFirst, cellule (section Paragraph)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.  <br/> |[IndLeft, cellule (section Paragraph)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Représente la distance entre chaque ligne du paragraphe et la marge droite du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.  <br/> |[IndRight, cellule (section Paragraph)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin.  <br/> |[SpAfter, cellule (section Paragraph)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.  <br/> |[SpBefore, cellule (section Paragraph)](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.  <br/> |[SpLine, cellule (section Paragraph)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Représente la distance entre la première ligne du paragraphe et la puce.  <br/> |[TextPosAfterBullet, cellule (section Paragraph)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

