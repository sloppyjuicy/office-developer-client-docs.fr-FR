---
title: Élément de cellule (remplissage dégradé Section) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.
ms.openlocfilehash: 3c4cdf1f60f68748fd2500b2dec0b5a5ad553ff5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386354"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a>Élément de cellule (remplissage dégradé Section) (« Visio XML »)

Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.
  
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
|[Row, élément (FillGradient Section)](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.  <br/> |
   
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
|GradientStopColor  <br/> |La valeur de la couleur du point de dégradé. Cette valeur peut être exprimée en tant que le numéro d’index d’une couleur dans la palette de document ou en utilisant les fonctions **RGB**, **THEMEVAL**ou **TSL** .  <br/> |[Ligne Point de dégradé (section Remplissage dégradé)](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |Le niveau de transparence du point de dégradé, sous forme de pourcentage.  <br/> |[Ligne Point de dégradé (section Remplissage dégradé)](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |La position du point de dégradé sur l’axe de dégradé ligne, sous forme de pourcentage à partir du point d’origine du dégradé à l’extrémité du dégradé.  <br/> |[Ligne Point de dégradé (section Remplissage dégradé)](gradient-stop-row-fill-gradient-section.md) <br/> |
   

