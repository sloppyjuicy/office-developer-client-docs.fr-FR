---
title: Élément maître (Masters_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contient des éléments qui définissent un masque du document.
ms.openlocfilehash: 51c5f0ad8bee5000e981fcfd4d15e2e49f2bda3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789075"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Élément maître (Masters_Type, complexType) (« Visio XML »)

Contient des éléments qui définissent un masque du document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Se connecte](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.  <br/> |
|[Icône](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Spécifie qu'un MIME (Multipurpose Internet Mail Extensions) codés icône binaire (au format .ico) d’un élément **Master** ou **MasterShortcut** dans un document.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contient des éléments qui définissent la feuille de page pour un élément de **Page** ou **Master** .  <br/> |
|Shapes  <br/> |Shapes_Type  <br/> |Contient une collection d’éléments de la **forme** .  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Spécifie si le texte de la forme de base dans la fenêtre de gabarit est aligné à gauche, à droite ou au centre.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|BaseID  <br/> |XSD : String  <br/> |facultatif  <br/> |Un GUID (identificateur global unique) qui identifie la forme de base dans les documents.  <br/> |Valeurs du type xsd : String.  <br/> |
|Hidden  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si la forme de base est masqué dans l’interface utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |La taille d’icône de l’élément.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si l’icône est automatiquement générée à partir de la forme de base.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Détermine comment Microsoft Visio déterminent que si un document maître est déjà présent lorsqu’une instance d’une forme de base est déplacé sur la page de dessin.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Le nom de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Détermine si une forme de base se comporte comme un motif personnalisé.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD : String  <br/> |facultatif  <br/> |La barre d’état et l’outil de Conseil invite pour l’élément.  <br/> |Valeurs du type xsd : String.  <br/> |
|UniqueID  <br/> |XSD : String  <br/> |facultatif  <br/> |GUID qui identifie la forme de base dans le document.  <br/> |Valeurs du type xsd : String.  <br/> |
   

