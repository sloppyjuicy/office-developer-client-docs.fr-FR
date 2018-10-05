---
title: Élément ProtectMasters (DocumentSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Spécifie si l’utilisateur est empêché de création, modification ou la suppression des formes de base. L’utilisateur peut toujours créer des nouvelles formes à partir d’une forme de base, quel que soit ce paramètre.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386445"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>Élément ProtectMasters (DocumentSettings_Type, complexType) (« Visio XML »)

Spécifie si l’utilisateur est empêché de création, modification ou la suppression des formes de base. L’utilisateur peut toujours créer des nouvelles formes à partir d’une forme de base, quel que soit ce paramètre. 
  
La plage de valeurs possibles pour cet élément est « 0 » ou « 1 ». Une valeur de « 0 » indique que les utilisateurs peuvent créer, modifier ou supprimer des formes de base. La valeur « 1 » indique que les utilisateurs ne peuvent pas créer, modifier ou supprimer des formes de base.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contient des éléments qui spécifient les paramètres de document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  

