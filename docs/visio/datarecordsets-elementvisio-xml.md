---
title: Élément DataRecordSets (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contient tous les éléments DataRecordset du document.
ms.openlocfilehash: 9593aa639913e93c95cac92c8e6ca1e02ea0d76f
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507111"
---
# <a name="datarecordsets-element-visio-xml"></a>Élément DataRecordSets (Visio XML)

Contient tous les **éléments DataRecordset** du document. 
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataRecordset** du document. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID du jeu d’enregistrements de données actif dans  la fenêtre Données externes à la fermeture de la fenêtre, afin qu’il puisse être restauré à la prochaine ouverture de la fenêtre. |Valeurs du type xsd:unsignedInt. |
|DataWindowOrder  <br/> |xsd:string  <br/> |facultatif  <br/> |Ordre des jeux d’enregistrements de données affichés dans les onglets de la **fenêtre Données** externes. Liste ordonnée d’ID de jeu d’enregistrements de données, séparés par des points-virgules. |Valeurs du type xsd:string. |
|NextID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID disponible suivant pour un nouveau recordset de données. |Valeurs du type xsd:unsignedInt. |
   

