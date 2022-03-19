---
title: Élément RefreshConflict (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données.
ms.openlocfilehash: aa1edcbe6384f90e2fb04b64401ce24db4e360dd
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634465"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a>Élément RefreshConflict (DataRecordSet_Type complexType) (Visio XML)

Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données.
  
## <a name="element-information"></a>Informations sur l'élément

| |Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de page de la forme impliquée dans le conflit. |Valeurs du type xsd:unsignedInt. |
|RowID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |L’ID de ligne d’origine de la ligne est maintenant en conflit après l’actualisation des données. |Valeurs du type xsd:unsignedInt. |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de forme de la forme impliquée dans le conflit. |Valeurs du type xsd:unsignedInt. |
   

