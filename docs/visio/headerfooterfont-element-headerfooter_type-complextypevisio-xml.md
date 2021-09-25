---
title: Élément HeaderFooterFont (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.
ms.openlocfilehash: a862141d12234efeaecdfe6976a1c19f18cbe6ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574152"
---
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>Élément HeaderFooterFont (HeaderFooter_Type complexType) (Visio XML)

Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contient des éléments pour l’en-tête et le pied de groupe d’un document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie le jeu de caractères de la police. Équivalent au champ GDI LOGFONTlfCharSet.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie la précision de découpage de la police. Équivalent au champ GDI LOGFONTlfClipPrecision.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Escapement  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie l’attribut d’escapement de la police. Équivalent au champ GDI LOGFONTlfEscapement.  <br/> |Valeurs du type xsd:int.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |facultatif  <br/> |Contient des informations sur une police.  <br/> |Valeurs du type xsd:string.  <br/> |
|Hauteur  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie la hauteur de la forme en unités de dessin.  <br/> |Valeurs du type xsd:int.  <br/> |
|Italic  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est en italique. Équivalent au champ GDI LOGFONTlfItalic.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Orientation  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie l’orientation de la police. Équivalent au champ GDI LOGFONTlfOrientation.  <br/> |Valeurs du type xsd:int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie l’attribut de précision de sortie de la police. Équivalent au champ GDI LOGFONTlfOutPrecision.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie l’emplacement et la famille de la police. Équivalent au champ GDI LOGFONTlfPitchAndFamily.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Qualité  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie la qualité de sortie de la police. Équivalent au champ GDI LOGFONTlfQuality.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est une police de type « strikeout ». Équivalent au champ GDI LOGFONTlfStrikeOut.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Souligner  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> |Spécifie si la police est soulignée. Équivalent au champ GDI LOGFONTlfUnderline.  <br/> |Valeurs du type xsd:unsignedByte.  <br/> |
|Pondération  <br/> |xsd:int  <br/> |facultatif  <br/> |Spécifie le poids de la police. Équivalent au champ GDI LOGFONTlfWeight.  <br/> |Valeurs du type xsd:int.  <br/> |
|Largeur  <br/> |xsd:int  <br/> |facultatif  <br/> |Contient la largeur de la forme associée en unités de dessin.  <br/> |Valeurs du type xsd:int.  <br/> |
   

