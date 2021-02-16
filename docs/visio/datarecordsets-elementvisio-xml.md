---
title: Élément DataRecordSets (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contient tous les éléments DataRecordset du document.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542442"
---
# <a name="datarecordsets-element-visio-xml"></a>Élément DataRecordSets (Visio XML)

Contient tous les **éléments DataRecordset** du document. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataRecordset** du document.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID du jeu d’enregistrements  de données actif dans la fenêtre Données externes à la fermeture de la fenêtre, afin qu’il puisse être restauré à la prochaine ouverture de la fenêtre.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |facultatif  <br/> |Ordre des jeux d’enregistrements de données affichés dans les onglets de la **fenêtre Données** externes. Liste ordonnée d’ID de jeu d’enregistrements de données, séparés par des points-virgules.  <br/> |Valeurs du type xsd:string.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID disponible suivant pour un nouveau recordset de données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

