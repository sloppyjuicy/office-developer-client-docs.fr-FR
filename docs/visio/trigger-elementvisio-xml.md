---
title: Élément Trigger (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Fournit des instructions pour Microsoft Visio recalcule une relation entre les parties de document dans un fichier Visio.
ms.openlocfilehash: a590ec1f9c19270f75d4d9e77804c0a7b45157b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385437"
---
# <a name="trigger-element-visio-xml"></a>Élément Trigger (« Visio XML »)

Fournit des instructions pour Microsoft Visio recalcule une relation entre les parties de document dans un fichier Visio.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master # .xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Spécifie les éléments de la cellule qui fournissent des informations pour la définition d’une forme.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Définit la structure DocumentSheet.  <br/> |
|[Feuille de style](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Représente un style défini dans un document.  <br/> |
|[PageSheet (Master_Type, complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés de la page de dessin associé à la forme de base.  <br/> |
|[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Spécifie les propriétés de la page de dessin associé à la page de dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une page de toa référence dans le dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> |Le nom de la formule à appeler lorsque le déclencheur est activé.  <br/> Consultez la section Notes.  <br/> |Valeurs du type xsd : String.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément **Trigger** doit être un ensemble limité de valeurs qui correspondent aux instructions de déclencheur. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément **Trigger** . 
  
|**Valeur**|**Élément parent**|**Description**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **HASCATEGORIES** .  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une page lorsqu’une référence croisée-composant à l’aide d’une **BKGPAGENAME,** fonction  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Un déclencheur qui s’affiche sur une page lorsque la page ou l’un de ses formes utilise une fonction **RGB** .  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un déclencheur qui apparaît dans un document lorsqu’il existe une référence croisée-composant à l’aide d’une **DOCCREATION,** fonction.  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **DATA1** .  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **DATA2** .  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **DATA3** .  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un déclencheur qui apparaît dans un document lorsqu’il existe une référence croisée-composant à l’aide d’une **doclastedit,** fonction.  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-partie à l’aide d’une fonction **ID** .  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une **MASTERNAME,** fonction.  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une **nom** de fonction.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Un déclencheur qui s’affiche sur une page si la page ou une de ses formes contenant ont une **maintenant** ou une fonction **RAND** .  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un déclencheur qui apparaît dans un document lorsqu’il existe une référence croisée-composant à l’aide d’une fonction **PAGECOUNT** .  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **PAGENAME** .  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une page lorsqu’une référence croisée-composant à l’aide d’une fonction **PAGENUMBER** .  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **POINTALONGPATH**, **PATHLENGTH**ou **PATHSEGMENT** .  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un déclencheur qui apparaît dans un document lorsqu’il existe une référence croisée-composant à l’aide d’une **DOCLASTPRINT,** fonction.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Un déclencheur qui apparaît dans un document lorsqu’il existe une référence croisée-composant à l’aide d’une **DOCLASTSAVE,** fonction.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche dans un document lorsqu’une référence croisée-composant à l’aide d’une fonction de la **catégorie**, **auteur**, **DESCRIPTION**, **mots clés**, **sujet**ou le **titre** .  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction de **TYPE** .  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une forme lorsqu’une référence croisée-composant à l’aide d’une fonction **CONTAINERMEMBERCOUNT** .  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type type complexe)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une page lorsqu’une référence croisée-composant à l’aide d’une fonction **CONTAINERSHEETREF** .  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Il existe un déclencheur qui s’affiche sur une page lorsqu’une référence croisée-composant à l’aide d’une fonction **POINTALONGPATH**, **PATHLENGTH**ou **PATHSEGMENT** .  <br/> |
   

