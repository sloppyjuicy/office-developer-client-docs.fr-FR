---
title: Élément PageSheet (Master_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Spécifie les propriétés de la page de dessin associé à la forme de base.
ms.openlocfilehash: 579b2b4f02c79a38842a150b8757329e19e7bb3a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399136"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>Élément PageSheet (Master_Type, complexType) (« Visio XML »)

Spécifie les propriétés de la page de dessin associé à la forme de base.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Forme de base](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Spécifie une forme de base dans un dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir duquel hériter de la mise en forme de remplissage. Il doit être la valeur de l’attribut **ID** associé à une **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir duquel hériter de la mise en forme de ligne. Il doit être la valeur de l’attribut **ID** associé à une **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la feuille de style à partir duquel hériter de la mise en forme de texte. Il doit être la valeur de l’attribut **ID** associé à une **StyleSheet_Type** dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |XSD : String  <br/> |facultatif  <br/> |ID unique de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd : String.  <br/> |
   

