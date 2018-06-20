---
title: Élément de cellule (ligne lien hypertexte) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788207"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Élément de cellule (ligne lien hypertexte) (« Visio XML »)

Contient les informations d’un lien hypertexte associé à une forme. Une forme contient une ligne **Hyperlink** pour chaque lien hypertexte. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Row, élément (Section liens hypertexte)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Contient les informations d’un lien hypertexte associé à une forme. Une forme contient une ligne **Hyperlink** pour chaque lien hypertexte.  <br/> |
   
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
|Address  <br/> |Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.  <br/> |[Address, cellule (section Hyperlinks)](address-cell-hyperlinks-section.md) <br/> |
|Default (Défaut)  <br/> |Détermine le lien hypertexte par défaut pour une forme ou une page.  <br/> |[Default, cellule (section Hyperlinks)](default-cell-hyperlinks-section.md) <br/> |
|Description  <br/> |Représente une chaîne de texte descriptive d’un lien hypertexte  <br/> |[Description, cellule (section Hyperlinks)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Représente une chaîne qui transmet les informations à utiliser dans la résolution d’une URL, comme les coordonnées d’une image interactive.  <br/> |[ExtraInfo, cellule (section Hyperlinks)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.  <br/> |[Frame, cellule (section Hyperlinks)](frame-cell-hyperlinks-section.md) <br/> |
|Invisible  <br/> |Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page.  <br/> |[Invisible, cellule (section Hyperlinks)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.  <br/> |[NewWindow, cellule (section Hyperlinks)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.  <br/> |[SortKey, cellule (section Hyperlinks)](sortkey-cell-hyperlinks-section.md) <br/> |
|Sous-adresse  <br/> |Indique un emplacement au sein du document cible vers lequel établir un lien.  <br/> |[SubAddress, cellule (section Hyperlinks)](subaddress-cell-hyperlinks-section.md) <br/> |
   

