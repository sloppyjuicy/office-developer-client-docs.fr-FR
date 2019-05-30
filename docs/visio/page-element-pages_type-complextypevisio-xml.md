---
title: Élément de page (Pages_Type, complexType) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contient des éléments qui définissent une page dans le document.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538024"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Élément de page (Pages_Type, complexType) (XML Visio)

Contient des éléments qui définissent une page dans le document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |pages. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contient les éléments de **page** pour le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page pour un élément de **page** .  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Arrière-plan  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indicateur signalant si la page est une page d’arrière-plan.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|BackPage  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de la page d’arrière-plan de cette page.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|Nom  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom de l’élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|ReviewerID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID du réviseur associé à la superposition de marques de révision.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’un nouvel affichage (fenêtre) présuppose lorsqu’il est ouvert au départ.  <br/> |Valeurs du type xsd: double.  <br/> |
|ViewCenterY  <br/> |xsd: double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’un nouvel affichage (fenêtre) présuppose lorsqu’il est ouvert au départ.  <br/> |Valeurs du type xsd: double.  <br/> |
|ViewScale  <br/> |xsd: double  <br/> |facultatif  <br/> |Facteur d’agrandissement par défaut à utiliser lors de l’ouverture d’une nouvelle vue (fenêtre) de la page. Par exemple, 1 = 100%; 1,5 = 150%, etc.  <br/> |Valeurs du type xsd: double.  <br/> |
   

