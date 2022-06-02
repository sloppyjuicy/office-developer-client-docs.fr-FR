---
title: Élément cell (Hyperlink Row) (Visio XML)
description: L’élément cell (Hyperlink Row) (Visio XML) contient les informations d’un seul lien hypertexte associé à une forme.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
ms.openlocfilehash: 80b7dd0eceaaf856dd46731b11df948581a2aa96
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853831"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Élément cell (Hyperlink Row) (Visio XML)

Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne **de lien hypertexte** pour chaque lien hypertexte. 
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (section Lien hypertexte)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne **de lien hypertexte** pour chaque lien hypertexte. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule prend la valeur d’une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de l’attribut **V** est la dernière valeur valide. |Chaîne de message d’erreur. |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée. |Formule. |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet. |Nom de la cellule ShapeSheet. Consultez la section Remarques ci-dessous. |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL. |Unités de la cellule. |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule. |Valeur de la cellule ShapeSheet. |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément **Cell** doit être l’un des ensembles limités de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** autorisées pour cet élément **Cell** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|Adresse  <br/> |Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder. |[Address, cellule (section Hyperlinks)](address-cell-hyperlinks-section.md) <br/> |
|Par défaut  <br/> |Détermine le lien hypertexte par défaut d'une forme ou d'une page. |[Default, cellule (section Hyperlinks)](default-cell-hyperlinks-section.md) <br/> |
|Description  <br/> |Représente une chaîne de texte descriptive d’un lien hypertexte |[Description, cellule (section Hyperlinks)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Représente une chaîne qui passe l'information à utiliser dans la résolution d'une URL, comme les coordonnées d'un point dans une image interactive. |[ExtraInfo, cellule (section Hyperlinks)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Cadre  <br/> |Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide. |[Frame, cellule (section Hyperlinks)](frame-cell-hyperlinks-section.md) <br/> |
|Invisible  <br/> |Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page. |[Invisible, cellule (section Hyperlinks)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre. |[NewWindow, cellule (section Hyperlinks)](newwindow-cell-hyperlinks-section.md) <br/> |
|Sortkey  <br/> |Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel. |[SortKey, cellule (section Hyperlinks)](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |Indique un emplacement au sein du document cible vers lequel établir un lien. |[SubAddress, cellule (section Hyperlinks)](subaddress-cell-hyperlinks-section.md) <br/> |
   

