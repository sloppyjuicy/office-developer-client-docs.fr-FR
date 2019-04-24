---
title: Élément Master (Masters_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contient des éléments qui définissent une forme de base pour le document.
ms.openlocfilehash: f6effa521b7c5ea69d41b6770ee2dbef61af097c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283964"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Élément Master (Masters_Type complexType) ('Visio XML')

Contient des éléments qui définissent une forme de base pour le document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Masters. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie une icône binaire codée MIME (Multipurpose Internet Mail Extensions) (au format. ico) pour un élément **Master** ou **MasterShortcut** dans un document.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page d'un élément **page** ou **Master** .  <br/> |
|Formes  <br/> |Shapes_Type  <br/> |Contient une collection d'éléments **Shape** .  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Indique si le texte de la forme de base dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|BaseID  <br/> |xsd: String  <br/> |facultatif  <br/> |GUID (globally unique identifier) qui identifie la forme de base dans les documents.  <br/> |Valeurs du type xsd: String.  <br/> |
|Masqué  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si la forme de base est masquée dans l'interface utilisateur.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|IconSize  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Taille de l'icône de l'élément.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si l'icône est générée automatiquement à partir de la forme de base proprement dite.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID unique de l'élément au sein de son élément parent.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|MatchByName  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Détermine comment Microsoft Visio décide si une forme de base de document est déjà présente lorsqu'une instance d'une forme de base est déposée sur la page de dessin.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|Nom  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom de l'élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom universel de l'élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|PatternFlags  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|Invite  <br/> |xsd: String  <br/> |facultatif  <br/> |Barre d'État et invite d'outils pour l'élément.  <br/> |Valeurs du type xsd: String.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |facultatif  <br/> |GUID qui identifie la forme de base dans le document.  <br/> |Valeurs du type xsd: String.  <br/> |
   

