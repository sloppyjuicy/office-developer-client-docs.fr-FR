---
title: Élément cell (Character Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Spécifie un attribut de mise en forme pour l’exécuter de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540083"
---
# <a name="cell-element-character-section-visio-xml"></a>Élément cell (Character Section) (Visio XML)

Spécifie un attribut de mise en forme pour l’exécuter de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (Character Section)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme pour l’exécuter de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point.  <br/> |
   
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
|AsianFont  <br/> |Contient l’éumération de la police utilisée pour mettre en forme une version de texte contenant des caractères asiatiques.  <br/> |[AsianFont, cellule (section Character)](asianfont-cell-character-section.md) <br/> |
|Cas  <br/> |Détermine la cas d’une utilisation du texte d’une forme.  <br/> |[Case, cellule (section Character)](case-cell-character-section.md) <br/> |
|Couleur  <br/> |Détermine la couleur utilisée pour l’exécuter de texte d’une forme.  <br/> |[Color, cellule (section Character)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Détermine le degré de transparence de la couleur d’utilisation du texte d’un calque ou d’une forme, de 0 (complètement opaque) à 1 (complètement transparent).  <br/> |Aucun.  <br/> |
|ComplexScriptFont  <br/> |Contient le numéro de la police utilisée pour mettre en forme une séquence de texte composée de caractères de script complexes.  <br/> |[ComplexScriptFont, cellule (section Character)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Taille de la police utilisée pour mettre en forme une séquence de texte composée de caractères de script complexes.  <br/> |[ComplexScriptSize, cellule (section Character)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Détermine si la plage d’une série de texte présente un double soulignement en dessous.  <br/> |[DoubleULine, cellule (section Character)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Détermine si une exécute de texte est mise en forme en tant que double strikethrough.  <br/> |[DoubleStrikethrough, cellule (section Character)](doublestrikethrough-cell-character-section.md) <br/> |
|Police  <br/> |Représente le numéro de la police utilisée pour mettre en forme une série de texte.  <br/> |[Font, cellule (section Character)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Spécifie la largeur de la police.  <br/> |Aucun.  <br/> |
|LangID  <br/> |Indique la langue dans laquelle une version de texte a été entrée.  <br/> |[LangID, cellule (section Character)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Spécifie la quantité d’espace entre deux caractères ou plus. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.  <br/> |Aucun.  <br/> |
|Overline  <br/> |Détermine si une ligne est au-dessus d’une ligne au-dessus d’une ligne de texte.  <br/> |[Overline, cellule (section Character)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Détermine la position de l’exécuter de texte d’une forme par rapport à la ligne de base.  <br/> |[Pos, cellule (section Character)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Détermine la taille d’un texte exécuté dans le bloc de texte de la forme.  <br/> |[Size, cellule (section Character)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Détermine si une version de texte est mise en forme comme une frappe.  <br/> |[Strikethru, cellule (section Character)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Indique la mise en forme des caractères appliquée à une plage d’un texte exécuté dans le bloc de texte de la forme.  <br/> |[Style, cellule (section Character)](style-cell-character-section.md) <br/> |
   

