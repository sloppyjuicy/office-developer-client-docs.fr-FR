---
title: Élément Page (Pages_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contient des éléments qui définissent une page dans le document.
ms.openlocfilehash: 12ccd628dc904aee4d9fc361021377ede8627f5e
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522666"
---
# <a name="page-element-pages_type-complextype-visio-xml"></a>Élément Page (Pages_Type complexType) (Visio XML)

Contient des éléments qui définissent une page dans le document.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contient les **éléments Page** du document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page d’un **élément Page** . |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Arrière-plan  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indicateur indiquant si la page est une page d’arrière-plan. |Valeurs du type xsd:boolean. |
|BackPage  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de la page d’arrière-plan de cette page. |Valeurs du type xsd:unsignedInt. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:unsignedInt. |
|IsCustomName  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur. |Valeurs du type xsd:Boolean. |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur. |Valeurs du type xsd:Boolean. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément. |Valeurs du type xsd:string. |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément. |Valeurs du type xsd:string. |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID du réviseur associé à la superposition de marques de contrôle. |Valeurs du type xsd:unsignedInt. |
|ViewCenterX  <br/> |xsd:double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’une nouvelle vue (fenêtre) suppose lorsqu’elle est ouverte initialement. |Valeurs du type xsd:double. |
|ViewCenterY  <br/> |xsd:double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’une nouvelle vue (fenêtre) suppose lorsqu’elle est ouverte initialement. |Valeurs du type xsd:double. |
|ViewScale  <br/> |xsd:double  <br/> |facultatif  <br/> |Facteur de grossissement par défaut à utiliser lors de l’ouverture d’un nouvel affichage (fenêtre) de la page. Par exemple, 1 = 100 %; 1,5 = 150 %, etc. |Valeurs du type xsd:double. |
   

