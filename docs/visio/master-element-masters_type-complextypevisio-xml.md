---
title: Élément Master (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contient des éléments qui définissent une base pour le document.
ms.openlocfilehash: fcb3729e1a749afd9b10252bfcaff4d12eb2d253
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771215"
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contient les **éléments Master** du document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin. |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie une icône binaire codée MIME (Multipurpose Internet Mail Extensions) (au format .ico) pour un élément **Master** ou **MasterShortcut** dans un document. |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page pour un **élément Page** **ou Master** . |
|Formes  <br/> |Shapes_Type  <br/> |Contient une collection **d’éléments Shape** . |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Spécifie si le texte de la maîtrise dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre. |Valeurs du type xsd:unsignedShort. |
|BaseID  <br/> |xsd:string  <br/> |facultatif  <br/> |GUID (identificateur global unique) qui identifie la forme de base dans tous les documents. |Valeurs du type xsd:string. |
|Hidden  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si la base est masquée dans l’interface utilisateur. |Valeurs du type xsd:boolean. |
|IconSize  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Taille de l’icône de l’élément. |Valeurs du type xsd:unsignedShort. |
|IconUpdate  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si l’icône est générée automatiquement à partir de la forme de forme de forme de passe elle-même. |Valeurs du type xsd:boolean. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:unsignedInt. |
|MatchByName  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Détermine comment Microsoft Visio si une forme de maître de document est déjà présente lorsqu’une instance d’une forme de passe est abandonnée sur la page de dessin. |Valeurs du type xsd:boolean. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément. |Valeurs du type xsd:string. |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément. |Valeurs du type xsd:string. |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé. |Valeurs du type xsd:unsignedShort. |
|Invite  <br/> |xsd:string  <br/> |facultatif  <br/> |Barre d’état et invite d’info-conseil pour l’élément. |Valeurs du type xsd:string. |
|UniqueID  <br/> |xsd:string  <br/> |facultatif  <br/> |GUID qui identifie la base dans le document. |Valeurs du type xsd:string. |
   

