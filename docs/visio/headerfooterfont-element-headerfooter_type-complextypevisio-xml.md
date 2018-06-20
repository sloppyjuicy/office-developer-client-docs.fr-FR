---
title: HeaderFooterFont, élément (HeaderFooter_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Spécifie la police utilisée pour le texte d’en-tête et pied de page.
ms.openlocfilehash: 249040702b1594cc650ccf1304ed7c1c79581ea3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788753"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>HeaderFooterFont, élément (HeaderFooter_Type, complexType) (« Visio XML »)

Spécifie la police utilisée pour le texte d’en-tête et pied de page.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contient les éléments d’en-tête et de pied de page d’un document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Jeu de caractères  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Spécifie le jeu de caractères de la police. Équivalent au champ LOGFONTlfCharSet GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Spécifie la précision de découpage de la police. Équivalent au champ LOGFONTlfClipPrecision GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Échappement  <br/> |XSD : int  <br/> |facultatif  <br/> |Spécifie l’attribut d’échappement de la police. Équivalent au champ LOGFONTlfEscapement GDI.  <br/> |Valeurs du type xsd : int.  <br/> |
|Nom de la police  <br/> |XSD : String  <br/> |facultatif  <br/> |Contient des informations sur une police.  <br/> |Valeurs du type xsd : String.  <br/> |
|Height  <br/> |XSD : int  <br/> |facultatif  <br/> |Spécifie la hauteur de la forme en unités de dessin.  <br/> |Valeurs du type xsd : int.  <br/> |
|Italique  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Indique si la police est en italique. Équivalent au champ LOGFONTlfItalic GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Orientation  <br/> |XSD : int  <br/> |facultatif  <br/> |Spécifie l’orientation de la police. Équivalent au champ LOGFONTlfOrientation GDI.  <br/> |Valeurs du type xsd : int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Spécifie l’attribut de précision de sortie de la police. Équivalent au champ LOGFONTlfOutPrecision GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Spécifie la hauteur et la famille de la police. Équivalent au champ LOGFONTlfPitchAndFamily GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Qualité  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Spécifie la qualité de sortie de la police. Équivalent au champ LOGFONTlfQuality GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Barré  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Indique si la police est une police barré. Équivalent au champ LOGFONTlfStrikeOut GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Souligné  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est soulignée. Équivalent au champ LOGFONTlfUnderline GDI.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Pondération  <br/> |XSD : int  <br/> |facultatif  <br/> |Spécifie l’épaisseur de la police. Équivalent au champ LOGFONTlfWeight GDI.  <br/> |Valeurs du type xsd : int.  <br/> |
|Width  <br/> |XSD : int  <br/> |facultatif  <br/> |Contient la largeur de la forme associée en unités de dessin.  <br/> |Valeurs du type xsd : int.  <br/> |
   

