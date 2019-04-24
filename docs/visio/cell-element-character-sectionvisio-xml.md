---
title: Élément de cellule (section caractères) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Spécifie un attribut de mise en forme pour la séquence de texte d'une forme, comme la police, la couleur, le style, la casse, la position par rapport à la ligne de base ou la taille du point.
ms.openlocfilehash: 6dd895b33353944d27abb0d64a6a6df64ca19896
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356083"
---
# <a name="cell-element-character-section-visio-xml"></a>Élément de cellule (section caractères) ('Visio XML')

Spécifie un attribut de mise en forme pour la séquence de texte d'une forme, comme la police, la couleur, le style, la casse, la position par rapport à la ligne de base ou la taille du point.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. xml, Master #. xml, page #. Xml  <br/> |
   
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
|[Élément de ligne (section caractères)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme pour la séquence de texte d'une forme, comme la police, la couleur, le style, la casse, la position par rapport à la ligne de base ou la taille du point.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur **E** est la valeur actuelle (chaîne de message d'erreur); la valeur de l'attribut **V** est la dernière valeur valide.  <br/> |Chaîne de message d'erreur.  <br/> |
|F  <br/> |xsd: String  <br/> |facultatif  <br/> | Représente la formule de l'élément. Cet attribut peut contenir l'une des chaînes suivantes:  <br/>  ' (une formule) 'si la formule existe localement  <br/>  `No Formula`Si la formule est supprimée ou bloquée localement  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Consultez la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente une unité de mesure la valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L'attribut **N** de cet élément de **cellule** doit correspondre à l'un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet. RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Value**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|AsianFont  <br/> |Contient l'énumération de la police utilisée pour mettre en forme une séquence de texte contenant des caractères asiatiques.  <br/> |[AsianFont, cellule (section Character)](asianfont-cell-character-section.md) <br/> |
|Cas  <br/> |Détermine la casse de la séquence de texte d'une forme.  <br/> |[Case, cellule (section Character)](case-cell-character-section.md) <br/> |
|Couleur  <br/> |Détermine la couleur utilisée pour l'exécution de texte d'une forme.  <br/> |[Color, cellule (section Character)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Détermine le degré de transparence de la couleur d'exécution du texte d'une forme ou d'une forme, de 0 (totalement opaque) à 1 (entièrement transparent).  <br/> |Aucun.  <br/> |
|ComplexScriptFont  <br/> |Contient le numéro de la police utilisée pour mettre en forme un texte composé de caractères de script complexes.  <br/> |[ComplexScriptFont, cellule (section Character)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Taille de la police utilisée pour mettre en forme un texte exécuté composé de caractères de script complexes.  <br/> |[ComplexScriptSize, cellule (section Character)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Détermine si la plage d'une séquence de texte est soulignée d'un double trait de soulignement.  <br/> |[DoubleULine, cellule (section Character)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Détermine si une séquence de texte est mise en forme barré double.  <br/> |[DoubleStrikethrough, cellule (section Character)](doublestrikethrough-cell-character-section.md) <br/> |
|Police  <br/> |Représente le numéro de la police utilisée pour mettre en forme une séquence de texte.  <br/> |[Font, cellule (section Character)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Spécifie la largeur de la police.  <br/> |Aucun.  <br/> |
|ID  <br/> |Indique la langue dans laquelle une séquence de texte a été entrée.  <br/> |[LangID, cellule (section Character)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Indique la quantité d'espace entre deux ou plusieurs caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.  <br/> |Aucun.  <br/> |
|Overline  <br/> |Détermine si une séquence de texte est dotée d'une ligne au-dessus.  <br/> |[Overline, cellule (section Character)](overline-cell-character-section.md) <br/> |
|TPV  <br/> |Détermine la position de la séquence de texte d'une forme par rapport à la ligne de base.  <br/> |[Pos, cellule (section Character)](pos-cell-character-section.md) <br/> |
|Taille  <br/> |Détermine la taille d'une séquence de texte dans le bloc de texte de la forme.  <br/> |[Size, cellule (section Character)](size-cell-character-section.md) <br/> |
|Barré  <br/> |Détermine si une séquence de texte est mise en forme barré.  <br/> |[Strikethru, cellule (section Character)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Indique la mise en forme de caractères appliquée à une plage d'une séquence de texte dans le bloc de texte d'une forme.  <br/> |[Style, cellule (section Character)](style-cell-character-section.md) <br/> |
   

