---
title: Élément MasterShortcut (Masters_Type complexType) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Spécifie un raccourci de forme de base défini dans le document.
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538206"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Élément MasterShortcut (Masters_Type complexType) (XML Visio)

Spécifie un raccourci de forme de base défini dans le document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Master #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contient les éléments de **forme de base** pour le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie une icône binaire codée MIME (Multipurpose Internet Mail Extensions) (au format. ico) pour un élément **Master** ou **MasterShortcut** dans un document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Indique si le texte de l’élément dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|IconSize  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Taille de l’icône de l’élément.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Nom  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom de l’élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|PatternFlags  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|Invite  <br/> |xsd: String  <br/> |facultatif  <br/> |Barre d’État et invite d’outils pour l’élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|ShortcutHelp  <br/> |xsd: String  <br/> |facultatif  <br/> |Chaîne d’aide pour l’élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|ShortcutURL  <br/> |xsd: String  <br/> |facultatif  <br/> |URL d’un élément **MasterShortcut** .  <br/> |Valeurs du type xsd: String.  <br/> |
   

