---
title: Élément HeaderFooterFont (complexType HeaderFooter_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.
ms.openlocfilehash: f14d973caddc77394881d1b1dfd62a43f10cd7bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322427"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>Élément HeaderFooterFont (complexType HeaderFooter_Type) ('Visio XML')

Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contient des éléments pour l'en-tête et le pied de page d'un document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Spécifie le jeu de caractères de la police. Équivalent au champ LOGFONTlfCharSet GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Spécifie la précision de découpage de la police. Équivalent au champ LOGFONTlfClipPrecision GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|Échappement  <br/> |xsd: int  <br/> |facultatif  <br/> |Spécifie l'attribut d'échappement de la police. Équivalent au champ LOGFONTlfEscapement GDI.  <br/> |Valeurs du type xsd: int.  <br/> |
|FaceName  <br/> |xsd: String  <br/> |facultatif  <br/> |Contient des informations sur une police.  <br/> |Valeurs du type xsd: String.  <br/> |
|Hauteur  <br/> |xsd: int  <br/> |facultatif  <br/> |Indique la hauteur de la forme en unités de dessin.  <br/> |Valeurs du type xsd: int.  <br/> |
|Italic  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Indique si la police est en italique. Équivalent au champ LOGFONTlfItalic GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|Orientation  <br/> |xsd: int  <br/> |facultatif  <br/> |Spécifie l'orientation de la police. Équivalent au champ LOGFONTlfOrientation GDI.  <br/> |Valeurs du type xsd: int.  <br/> |
|La précision  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Spécifie l'attribut de précision de sortie de la police. Équivalent au champ LOGFONTlfOutPrecision GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Spécifie la hauteur et la largeur de la police. Équivalent au champ LOGFONTlfPitchAndFamily GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|Quality  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Spécifie la qualité de sortie de la police. Équivalent au champ LOGFONTlfQuality GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|Barré  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Indique si la police est barrée. Équivalent au champ LOGFONTlfStrikeOut GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|Underline  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> |Indique si la police est soulignée. Équivalent au champ LOGFONTlfUnderline GDI.  <br/> |Valeurs du type xsd: unsignedByte.  <br/> |
|Pondération  <br/> |xsd: int  <br/> |facultatif  <br/> |Spécifie l'épaisseur de la police. Équivalent au champ LOGFONTlfWeight GDI.  <br/> |Valeurs du type xsd: int.  <br/> |
|Largeur  <br/> |xsd: int  <br/> |facultatif  <br/> |Contient la largeur de la forme associée en unités de dessin.  <br/> |Valeurs du type xsd: int.  <br/> |
   

