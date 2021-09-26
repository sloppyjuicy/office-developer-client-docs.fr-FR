---
title: Élément MasterShortcut (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Spécifie un raccourci maître défini dans le document.
ms.openlocfilehash: b3be61ce7f9b82e1187dee6ee26bc6b3f92a6e07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627911"
---
# <a name="mastershortcut-element-masters_type-complextype-visio-xml"></a>Élément MasterShortcut (Masters_Type complexType) (Visio XML)

Spécifie un raccourci maître défini dans le document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contient les **éléments Master** du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie une icône binaire codée MIME (Multipurpose Internet Mail Extensions) (au format .ico) pour un élément **Master** ou **MasterShortcut** dans un document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Spécifie si le texte de l’élément dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Taille de l’icône de l’élément.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Invite  <br/> |xsd:string  <br/> |facultatif  <br/> |Barre d’état et invite d’info-conseil pour l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|ShortcutHelp  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne d’aide pour l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|ShortcutURL  <br/> |xsd:string  <br/> |facultatif  <br/> |URL d’un **élément MasterShortcut.**  <br/> |Valeurs du type xsd:string.  <br/> |
   

