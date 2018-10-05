---
title: HeaderFooter, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Contient les éléments d’en-tête et de pied de page d’un document.
ms.openlocfilehash: eabb19100c4b37a546c0a271cfba5a0c865a7e83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384443"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a>HeaderFooter, élément (VisioDocument_Type, complexType) (« Visio XML »)

Contient les éléments d’en-tête et de pied de page d’un document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |L’élément racine d’un document Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[FooterCenter](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterCenter_Type](footercenter_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie centrale du pied de page d’un document.  <br/> |
|[FooterLeft](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterLeft_Type](footerleft_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie gauche du pied de page d’un document.  <br/> |
|[FooterMargin](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterMargin_Type](footermargin_type-complextypevisio-xml.md) <br/> |Indique la marge du pied de page d’un document.  <br/> |
|[FooterRight](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterRight_Type](footerright_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie droite du pied de page d’un document.  <br/> |
|[HeaderCenter](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderCenter_Type](headercenter_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie centrale de l’en-tête d’un document.  <br/> |
|[HeaderFooterFont](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |Spécifie la police utilisée pour le texte d’en-tête et pied de page.  <br/> |
|[HeaderLeft](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderLeft_Type](headerleft_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie gauche de l’en-tête d’un document.  <br/> |
|[HeaderMargin](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderMargin_Type](headermargin_type-complextypevisio-xml.md) <br/> |Indique la marge de l’en-tête d’un document.  <br/> |
|[HeaderRight](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderRight_Type](headerright_type-complextypevisio-xml.md) <br/> |Contient la chaîne de texte qui apparaît dans la partie droite de l’en-tête d’un document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|HeaderFooterColor  <br/> |XSD : String  <br/> |facultatif  <br/> |La valeur RVB de la couleur du texte de l’en-tête et le pied de page au format hexadécimal ; par exemple, #rrggbb.  <br/> |Valeurs du type xsd : String.  <br/> |
   

