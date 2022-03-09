---
title: Élément HeaderFooterFont (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.
ms.openlocfilehash: 57fd3988a55d94877e138dc76c02dcf6752ae0a3
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404784"
---
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>Élément HeaderFooterFont (HeaderFooter_Type complexType) (Visio XML)

Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contient des éléments pour l’en-tête et le pied de groupe d’un document. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie le jeu de caractères de la police. Équivalent au champ GDI LOGFONTlfCharSet. |Valeurs du type xsd:unsignedByte. |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie la précision de découpage de la police. Équivalent au champ GDI LOGFONTlfClipPrecision. |Valeurs du type xsd:unsignedByte. |
|Escapement  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie l’attribut d’escapement de la police. Équivalent au champ GDI LOGFONTlfEscapement. |Valeurs du type xsd:int. |
|FaceName  <br/> |xsd:string  <br/> |facultatif  <br/> |Contient des informations sur une police. |Valeurs du type xsd:string. |
|Hauteur  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie la hauteur de la forme en unités de dessin. |Valeurs du type xsd:int. |
|Italic  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est en italique. Équivalent au champ GDI LOGFONTlfItalic. |Valeurs du type xsd:unsignedByte. |
|Orientation  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie l’orientation de la police. Équivalent au champ GDI LOGFONTlfOrientation. |Valeurs du type xsd:int. |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie l’attribut de précision de sortie de la police. Équivalent au champ GDI LOGFONTlfOutPrecision. |Valeurs du type xsd:unsignedByte. |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie l’emplacement et la famille de la police. Équivalent au champ GDI LOGFONTlfPitchAndFamily. |Valeurs du type xsd:unsignedByte. |
|Qualité  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie la qualité de sortie de la police. Équivalent au champ GDI LOGFONTlfQuality. |Valeurs du type xsd:unsignedByte. |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est une police de type « strikeout ». Équivalent au champ GDI LOGFONTlfStrikeOut. |Valeurs du type xsd:unsignedByte. |
|Souligner  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est soulignée. Équivalent au champ GDI LOGFONTlfUnderline. |Valeurs du type xsd:unsignedByte. |
|Pondération  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie le poids de la police. Équivalent au champ GDI LOGFONTlfWeight. |Valeurs du type xsd:int. |
|Largeur  <br/> |xsd:int  <br/> |facultatif  <br/> |Contient la largeur de la forme associée en unités de dessin. |Valeurs du type xsd:int. |
   

