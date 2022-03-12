---
title: Élément MasterShortcut (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Spécifie un raccourci maître défini dans le document.
ms.openlocfilehash: 439dd57fe69e46e48bb4f196c454df68320024d6
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448481"
---
# <a name="mastershortcut-element-masters_type-complextype-visio-xml"></a>Élément MasterShortcut (Masters_Type complexType) (Visio XML)

Spécifie un raccourci maître défini dans le document.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contient les **éléments Master** du document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie une icône binaire codée MIME (Multipurpose Internet Mail Extensions) (au format .ico) pour un élément **Master** ou **MasterShortcut** dans un document. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Spécifie si le texte de l’élément dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre. |Valeurs du type xsd:unsignedShort. |
|IconSize  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Taille de l’icône de l’élément. |Valeurs du type xsd:unsignedShort. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:unsignedInt. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément. |Valeurs du type xsd:string. |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément. |Valeurs du type xsd:string. |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé. |Valeurs du type xsd:unsignedShort. |
|Invite  <br/> |xsd:string  <br/> |facultatif  <br/> |Barre d’état et invite d’info-conseil pour l’élément. |Valeurs du type xsd:string. |
|ShortcutHelp  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne d’aide pour l’élément. |Valeurs du type xsd:string. |
|ShortcutURL  <br/> |xsd:string  <br/> |facultatif  <br/> |URL d’un **élément MasterShortcut** . |Valeurs du type xsd:string. |
   

