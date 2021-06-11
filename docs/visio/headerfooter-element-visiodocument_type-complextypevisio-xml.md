---
title: Élément HeaderFooter (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Contient des éléments pour l’en-tête et le pied de groupe d’un document.
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541105"
---
# <a name="headerfooter-element-visiodocument_type-complextype-visio-xml"></a>Élément HeaderFooter (VisioDocument_Type complexType) (Visio XML)

Contient des éléments pour l’en-tête et le pied de groupe d’un document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[FooterCenter](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterCenter_Type](footercenter_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie centrale du pied de ligne d’un document.  <br/> |
|[FooterLeft](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterLeft_Type](footerleft_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie gauche du pied de groupe d’un document.  <br/> |
|[FooterMargin](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterMargin_Type](footermargin_type-complextypevisio-xml.md) <br/> |Spécifie la marge du pied de document.  <br/> |
|[FooterRight](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterRight_Type](footerright_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie droite du pied de groupe d’un document.  <br/> |
|[HeaderCenter](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderCenter_Type](headercenter_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît au centre de l’en-tête d’un document.  <br/> |
|[HeaderFooterFont](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.  <br/> |
|[HeaderLeft](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderLeft_Type](headerleft_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie gauche de l’en-tête d’un document.  <br/> |
|[HeaderMargin](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderMargin_Type](headermargin_type-complextypevisio-xml.md) <br/> |Spécifie la marge de l’en-tête d’un document.  <br/> |
|[HeaderRight](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderRight_Type](headerright_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie droite de l’en-tête d’un document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|HeaderFooterColor  <br/> |xsd:string  <br/> |facultatif  <br/> |Valeur RVB de la couleur du texte pour l’en-tête et le pied de groupe en notation hexadécimale ; par exemple, #rrggbb.  <br/> |Valeurs du type xsd:string.  <br/> |
   

