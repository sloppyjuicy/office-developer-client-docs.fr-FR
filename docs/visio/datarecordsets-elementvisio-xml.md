---
title: DataRecordSets, élément ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contient tous les éléments DataRecordset dans le document.
ms.openlocfilehash: 7730e55f0025181db193a1e64226e879f9072e90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360325"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets, élément ('Visio XML')

Contient tous les éléments **DataRecordset** dans le document. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |recordsets. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contient tous les éléments **DataRecordset** dans le document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID du jeu d'enregistrements de données actif dans la fenêtre **données externes** lorsque la fenêtre se ferme, afin qu'elle puisse être restaurée la prochaine fois que la fenêtre s'ouvre.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd: String  <br/> |facultatif  <br/> |Ordre des jeux d'enregistrements de données affichés sous les onglets de la fenêtre **données externes** . Liste triée d'ID de jeu d'enregistrements de données, séparés par des points-virgules.  <br/> |Valeurs du type xsd: String.  <br/> |
|NextID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID suivant disponible pour un nouveau jeu d'enregistrements de données.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

