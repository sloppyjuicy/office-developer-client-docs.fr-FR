---
title: Élément ProtectMasters (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Spécifie si l’utilisateur ne peut pas créer, modifier ou supprimer des formes de base. L’utilisateur peut toujours créer de nouvelles formes à partir d’une forme de base, quel que soit ce paramètre.
ms.openlocfilehash: e0919e57bbdda5782548636793ba1ebb3744d788
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623172"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a>Élément ProtectMasters (DocumentSettings_Type complexType) (Visio XML)

Spécifie si l’utilisateur ne peut pas créer, modifier ou supprimer des formes de base. L’utilisateur peut toujours créer de nouvelles formes à partir d’une forme de base, quel que soit ce paramètre. 
  
La plage de valeurs possibles pour cet élément est « 0 » ou « 1 ». La valeur « 0 » indique que les utilisateurs peuvent créer, modifier ou supprimer des formes de base. La valeur « 1 » indique que les utilisateurs ne peuvent pas créer, modifier ou supprimer des formes de base.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contient des éléments qui spécifient les paramètres de document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  

