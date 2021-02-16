---
title: Élément Master (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contient des éléments qui définissent une base pour le document.
ms.openlocfilehash: 83727b89eaf44aae5dddecacff1f05f369ee0bf0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538045"
---
# <a name="master-element-masters_type-complextype-visio-xml"></a>Élément Master (Masters_Type complexType) (Visio XML)

Contient des éléments qui définissent une base pour le document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contient les **éléments Master** du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un **élément Connect** pour chaque connexion entre deux formes dans un dessin.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie une icône binaire codée MIME (Multipurpose Internet Mail Extensions) (au format .ico) pour un élément **Master** ou **MasterShortcut** dans un document.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page pour un **élément Page** **ou Master.**  <br/> |
|Formes  <br/> |Shapes_Type  <br/> |Contient une collection **d’éléments Shape.**  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Spécifie si le texte de la maîtrise dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd:string  <br/> |facultatif  <br/> |GUID (identificateur global unique) qui identifie la forme de base dans tous les documents.  <br/> |Valeurs du type xsd:string.  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si la base est masquée dans l’interface utilisateur.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Taille de l’icône de l’élément.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si l’icône est générée automatiquement à partir de la forme de forme de forme de passe elle-même.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Détermine comment Microsoft Visio détermine si une forme de maître de document est déjà présente lorsqu’une instance d’une forme de passe est abandonnée sur la page de dessin.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Invite  <br/> |xsd:string  <br/> |facultatif  <br/> |Barre d’état et invite d’info-conseil pour l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |GUID qui identifie la base dans le document.  <br/> |Valeurs du type xsd:string.  <br/> |
   

