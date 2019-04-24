---
title: Élément RefreshConflict (complexType DataRecordSet_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indique une ligne du jeu d'enregistrements de données qui est liée à une forme en conflit après l'actualisation du jeu d'enregistrements de données.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360136"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>Élément RefreshConflict (complexType DataRecordSet_Type) ('Visio XML')

Indique une ligne du jeu d'enregistrements de données qui est liée à une forme en conflit après l'actualisation du jeu d'enregistrements de données.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |recordsets. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID de la forme impliquée dans le conflit.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|RowID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |L'ID de ligne d'origine de la ligne est maintenant en conflit après l'actualisation des données.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ShapeID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID de la forme impliquée dans le conflit.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

