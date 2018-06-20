---
title: Élément de cellule (Section Character) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Spécifie un attribut de mise en forme de la séquence de texte d’une forme, comme la police, la couleur, de style, cas, la position relative à la ligne de base ou taille en points.
ms.openlocfilehash: 0d0725ec6ff19104d95780dcfbb3fff9715cbe92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788198"
---
# <a name="cell-element-character-section-visio-xml"></a>Élément de cellule (Section Character) (« Visio XML »)

Spécifie un attribut de mise en forme de la séquence de texte d’une forme, comme la police, la couleur, de style, cas, la position relative à la ligne de base ou taille en points.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Row, élément (Section Character)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme de la séquence de texte d’une forme, comme la police, la couleur, de style, cas, la position relative à la ligne de base ou taille en points.  <br/> |
   
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
|AsianFont  <br/> |Contient l’énumération de la police utilisée pour mettre en forme une séquence de texte contenant les caractères d’Asie orientale.  <br/> |[AsianFont, cellule (section Character)](asianfont-cell-character-section.md) <br/> |
|Cas  <br/> |Détermine la casse du texte d’une forme s’exécuter.  <br/> |[Case, cellule (section Character)](case-cell-character-section.md) <br/> |
|Couleur  <br/> |Détermine la couleur utilisée pour la séquence de texte d’une forme.  <br/> |[Color, cellule (section Character)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Détermine le degré de transparence d’un calque ou le texte de la forme exécution couleur, comprise entre 0 (complètement opaque) et 1 (complètement transparent).  <br/> |Aucun.  <br/> |
|ComplexScriptFont  <br/> |Contient le numéro de la police utilisée pour mettre en forme une séquence de texte composé de caractères de script complexe.  <br/> |[ComplexScriptFont, cellule (section Character)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |La taille de la police utilisée pour mettre en forme un texte exécuter composé de caractères de script complexe.  <br/> |[ComplexScriptSize, cellule (section Character)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Détermine si la plage d’une séquence de texte est souligné en double.  <br/> |[DoubleULine, cellule (section Character)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Détermine si une séquence de texte est barrée double.  <br/> |[DoubleStrikethrough, cellule (section Character)](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Représente le numéro de la police utilisée pour mettre en forme une séquence de texte.  <br/> |[Font, cellule (section Character)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Spécifie la largeur de la police.  <br/> |Aucun.  <br/> |
|ID de langue  <br/> |Indique la langue dans laquelle une séquence de texte a été entrée.  <br/> |[LangID, cellule (section Character)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Spécifie la quantité d’espace entre deux ou plusieurs caractères. Espace permettre être ajouté ou supprimé par incréments de 1/20 point.  <br/> |Aucun.  <br/> |
|Overline  <br/> |Détermine si une séquence de texte est surmonté d’un trait.  <br/> |[Overline, cellule (section Character)](overline-cell-character-section.md) <br/> |
|POS  <br/> |Détermine la position du texte d’une forme exécuter par rapport à la ligne de base.  <br/> |[Pos, cellule (section Character)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Détermine la taille du texte dans le bloc de texte.  <br/> |[Size, cellule (section Character)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Détermine si une séquence de texte est barrée.  <br/> |[Strikethru, cellule (section Character)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Indique la mise en forme de caractère appliqué à une plage de texte s’exécutent dans le bloc de texte.  <br/> |[Style, cellule (section Character)](style-cell-character-section.md) <br/> |
   

