---
title: Élément RefreshConflict (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indique une ligne dans le jeu d’enregistrements de données liée à une forme qui est en conflit après l’actualisation du jeu d’enregistrements.
ms.openlocfilehash: 0bcfb38c1a9ef84fc8581476fcce13b0de32c308
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789416"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>Élément RefreshConflict (DataRecordSet_Type, complexType) (« Visio XML »)

Indique une ligne dans le jeu d’enregistrements de données liée à une forme qui est en conflit après l’actualisation du jeu d’enregistrements.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |recordsets.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID de page de la forme impliquée dans le conflit.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RowID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’ID de ligne d’origine de la ligne en conflit après l’actualisation de données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID de la forme de la forme impliquée dans le conflit.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

