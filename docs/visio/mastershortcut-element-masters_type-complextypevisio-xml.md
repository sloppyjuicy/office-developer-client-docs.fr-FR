---
title: MasterShortcut, élément (Masters_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Spécifie un raccourci de base défini dans le document.
ms.openlocfilehash: be3e7d207e58d8c249598a7e156356d4f9e61849
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789081"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>MasterShortcut, élément (Masters_Type, complexType) (« Visio XML »)

Spécifie un raccourci de base défini dans le document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |maître # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Formes de base](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contient les éléments de la **forme de base** pour le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Icône](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie qu'un MIME (Multipurpose Internet Mail Extensions) codés icône binaire (au format .ico) d’un élément **Master** ou **MasterShortcut** dans un document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Spécifie si le texte de l’élément dans la fenêtre de gabarit est aligné à gauche, à droite ou centre.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |La taille d’icône de l’élément.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Le nom de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD : String  <br/> |facultatif  <br/> |La barre d’état et l’outil de Conseil invite pour l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|ShortcutHelp  <br/> |XSD : String  <br/> |facultatif  <br/> |Une chaîne d’aide pour l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|ShortcutURL  <br/> |XSD : String  <br/> |facultatif  <br/> |URL d’un élément **MasterShortcut** .  <br/> |Valeurs du type xsd : String.  <br/> |
   

