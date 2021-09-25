---
title: Élément DataRecordSets (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contient tous les éléments DataRecordset du document.
ms.openlocfilehash: 2465739067d0103e6e90cbb18c1cef6fc251732e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608262"
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
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID du jeu d’enregistrements  de données actif dans la fenêtre Données externes lorsque la fenêtre se ferme, afin qu’il puisse être restauré à la prochaine ouverture de la fenêtre.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |facultatif  <br/> |Ordre des jeux d’enregistrements de données affichés dans les onglets de la **fenêtre Données** externes. Liste ordonnée des ID de jeu d’enregistrements de données, séparés par des points-virgules.  <br/> |Valeurs du type xsd:string.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID disponible suivant pour un nouveau recordset de données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

