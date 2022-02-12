---
title: Élément Trigger (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Fournit des instructions à Microsoft Visio pour recalculer une relation entre les composants de document dans Visio fichier.
ms.openlocfilehash: cdb6d60069d4f1a72ac3c0ad68c0b899d31c7bf0
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784523"
---
# <a name="trigger-element-visio-xml"></a>Élément Trigger (Visio XML)

Fournit des instructions à Microsoft Visio pour recalculer une relation entre les composants de document dans Visio fichier.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie les éléments de cellule qui fournissent des informations pour la définition d’une forme. |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Définit la structure de la feuille de document. |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Représente un style défini dans un document. |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés de la page de dessin associée à la page de dessin. |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés de la page de dessin associée à la page de dessin. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page dans le dessin. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom de la formule à appeler lorsque le déclencheur est activé. Voir la section Remarques. |Valeurs du type xsd:string. |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Trigger** doit faire partie d’un ensemble limité de valeurs qui correspondent aux instructions de déclenchement. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Trigger** . 
  
|**Valeur**|**Élément parent**|**Description**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide d’une **fonction HASCATEGORIES** . |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page chaque fois que la page ou l’une de ses formes contenues utilise une **fonction RVB** . |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction DOCCREATION** . |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide **d’une fonction DATA1** . |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide **d’une fonction DATA2** . |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence à plusieurs éléments à l’aide **d’une fonction DATA3** . |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction DOCLASTEDIT** . |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence à plusieurs éléments à l’aide **d’une fonction ID** . |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide d’une **fonction MASTERNAME** . |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide **d’une fonction NAME** . |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page si la page ou l’une de ses formes contenantes a une fonction **NOW** ou **RAND** . |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’il existe une référence à plusieurs éléments à l’aide **d’une fonction PAGECOUNT** . |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide d’une **fonction PAGENAME** . |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’il existe une référence à plusieurs éléments à l’aide **d’une fonction PAGENUMBER** . |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence en plusieurs partie à l’aide d’une fonction **POINTALONGPATH**, **PATHLENGTH** ou **PATHSEGMENT** . |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction DOCLASTPRINT** . |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction DOCLASTSAVE** . |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’il existe une référence à plusieurs éléments à l’aide d’une fonction **CATEGORY**, **CREATOR**, **DESCRIPTION**, **KEYWORDS**, **SUBJECT** ou **TITLE** . |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence à plusieurs éléments à l’aide **d’une fonction TYPE** . |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction CONTAINERMEMBERCOUNT** . |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’il existe une référence à plusieurs éléments à l’aide d’une **fonction CONTAINERSHEETREF** . |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’il existe une référence à plusieurs éléments à l’aide d’une fonction **POINTALONGPATH**, **PATHLENGTH** ou **PATHSEGMENT** . |
   

