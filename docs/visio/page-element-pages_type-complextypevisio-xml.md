---
title: Élément de page (Pages_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contient des éléments qui définissent une page dans le document.
ms.openlocfilehash: 368c50a25a09d5f4fd808f3f019b074b7f6d246d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789191"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Élément de page (Pages_Type, complexType) (« Visio XML »)

Contient des éléments qui définissent une page dans le document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |pages.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contient les éléments de **Page** du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page pour un élément de **Page** .  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Arrière-plan  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indicateur signalant si la page est une page d’arrière-plan.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|BackPage  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID de la page d’arrière-plan de cette page.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IsCustomNameU  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Le nom de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|ReviewerID  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID du relecteur associé à la superposition.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD : double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’un nouvel affichage (fenêtre) lorsqu’il est ouvert à l’origine.  <br/> |Valeurs du type xsd : double.  <br/> |
|ViewCenterY  <br/> |XSD : double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’un nouvel affichage (fenêtre) lorsqu’il est ouvert à l’origine.  <br/> |Valeurs du type xsd : double.  <br/> |
|ViewScale  <br/> |XSD : double  <br/> |facultatif  <br/> |Le facteur d’agrandissement par défaut à utiliser lors de l’ouverture d’un nouvel affichage (fenêtre) de la page. Par exemple, 1 = 100 %. 1,5 = 150 % et ainsi de suite.  <br/> |Valeurs du type xsd : double.  <br/> |
   

