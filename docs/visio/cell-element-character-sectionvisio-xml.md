---
title: Élément cell (Character Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Spécifie un attribut de mise en forme pour l’écriture de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point.
ms.openlocfilehash: 1ef32dceee6fd0e5d21a12af196e0cfecdbff322
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788947"
---
# <a name="cell-element-character-section-visio-xml"></a>Élément cell (Character Section) (Visio XML)

Spécifie un attribut de mise en forme pour l’écriture de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point.
  
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (Character Section)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme pour l’écriture de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
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
|AsianFont  <br/> |Contient l’éumération de la police utilisée pour mettre en forme une version de texte contenant des caractères asiatiques. |[AsianFont, cellule (section Character)](asianfont-cell-character-section.md) <br/> |
|Cas  <br/> |Détermine la cas d’une utilisation du texte d’une forme. |[Case, cellule (section Character)](case-cell-character-section.md) <br/> |
|Couleur  <br/> |Détermine la couleur utilisée pour l’exécuter de texte d’une forme. |[Color, cellule (section Character)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Détermine le degré de transparence de la couleur d’utilisation du texte d’une couche ou d’une forme, de 0 (complètement opaque) à 1 (complètement transparent). |Aucun. |
|ComplexScriptFont  <br/> |Contient le numéro de la police utilisée pour mettre en forme une séquence de texte composée de caractères de script complexes. |[ComplexScriptFont, cellule (section Character)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Taille de la police utilisée pour mettre en forme une séquence de texte composée de caractères de script complexes. |[ComplexScriptSize, cellule (section Character)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Détermine si la plage d’une série de texte présente un double soulignement en dessous. |[DoubleULine, cellule (section Character)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Détermine si une exécute de texte est mise en forme en tant que double strikethrough. |[DoubleStrikethrough, cellule (section Character)](doublestrikethrough-cell-character-section.md) <br/> |
|Police  <br/> |Représente le numéro de la police utilisée pour mettre en forme une série de texte. |[Font, cellule (section Character)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Spécifie la largeur de la police. |Aucun. |
|LangID  <br/> |Indique la langue dans laquelle une version de texte a été entrée. |[LangID, cellule (section Character)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Spécifie la quantité d’espace entre deux caractères ou plus. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point. |Aucun. |
|Overline  <br/> |Détermine si une ligne est au-dessus d’une ligne au-dessus d’une exécuter de texte. |[Overline, cellule (section Character)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Détermine la position de l’exécuter de texte d’une forme par rapport à la ligne de base. |[Pos, cellule (section Character)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Détermine la taille d’un texte exécuté dans le bloc de texte de la forme. |[Size, cellule (section Character)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Détermine si une exécute de texte est mise en forme comme une frappe. |[Strikethru, cellule (section Character)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Indique la mise en forme de caractères appliquée à une plage de texte exécuté dans le bloc de texte de la forme. |[Style, cellule (section Character)](style-cell-character-section.md) <br/> |
   

