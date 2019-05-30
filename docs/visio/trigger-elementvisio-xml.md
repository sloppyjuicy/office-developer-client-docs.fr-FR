---
title: Élément Trigger (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Fournit des instructions à Microsoft Visio pour recalculer une relation entre des parties de document dans un fichier Visio.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542904"
---
# <a name="trigger-element-visio-xml"></a>Élément Trigger (Visio XML)

Fournit des instructions à Microsoft Visio pour recalculer une relation entre des parties de document dans un fichier Visio.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Master #. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie les éléments Cell qui fournissent des informations sur la définition d’une forme.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Définit la structure DocumentSheet.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Représente un style défini dans un document.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie les propriétés de la page de dessin associée à la forme de base.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie les propriétés de la page de dessin associée à la page de dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une page de TOA de référence dans le dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Nom de la formule à appeler lorsque le déclencheur est activé.  <br/> Consultez la section Remarques.  <br/> |Valeurs du type xsd: String.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément **Trigger** doit correspondre à l’un des jeux de valeurs limités qui correspondent aux instructions de Trigger. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément **Trigger** . 
  
|**Valeur**|**Élément parent**|**Description**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre les composants à l’aide d’une fonction **HASCATEGORIES** existe.  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’une référence entre les composants à l’aide d’une fonction **BKGPAGENAME** existe.  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page chaque fois que la page ou l’une de ses formes contenues utilise une fonction **RGB** .  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’une référence entre les composants à l’aide d’une fonction **DOCCREATION** existe.  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre plusieurs parties utilisant une fonction **Data1** existe.  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre plusieurs parties est utilisée à l’aide d’une fonction **data2** .  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre les composants à l’aide de la fonction **data3** existe.  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’une référence entre les composants à l’aide d’une fonction **DOCLASTEDIT** existe.  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre plusieurs parties utilisant une fonction **ID** existe.  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre les composants à l’aide d’une fonction **MASTERNAME** existe.  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence intersites à l’aide d’une fonction **Name** existe.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page si la page ou l’une de ses formes contenant a une fonction de **Rand** ou **maintenant** .  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’une référence entre plusieurs parties utilisant une fonction **PageCount** existe.  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre les composants à l’aide de la fonction **pagename** existe.  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’une référence entre les composants à l’aide d’une fonction **PAGENUMBER** existe.  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre les composants à l’aide d’une fonction **POINTALONGPATH**, **PATHLENGTH**ou **PATHSEGMENT** existe.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’une référence entre les composants à l’aide d’une fonction **DOCLASTPRINT** existe.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur un document lorsqu’une référence entre les composants à l’aide d’une fonction **DOCLASTSAVE** existe.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît dans un document lorsqu’une référence entre les composants à l’aide d’une fonction **Category**, **Creator**, **Description**, Keywords, **Subject**ou **title** existe. ****  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre plusieurs parties utilisant une fonction **type** existe.  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une forme lorsqu’une référence entre les composants à l’aide d’une fonction **CONTAINERMEMBERCOUNT** existe.  <br/> |
|Zorderchanged,  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’une référence entre les composants à l’aide d’une fonction **CONTAINERSHEETREF** existe.  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Déclencheur qui apparaît sur une page lorsqu’une référence entre les composants à l’aide d’une fonction **POINTALONGPATH**, **PATHLENGTH**ou **PATHSEGMENT** existe.  <br/> |
   

