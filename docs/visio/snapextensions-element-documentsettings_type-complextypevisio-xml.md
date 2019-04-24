---
title: Élément SnapExtensions (complexType DocumentSettings_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Indique si un paramètre d'extension d'alignement spécifique est activé ou désactivé pour la fenêtre active.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334530"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Élément SnapExtensions (complexType DocumentSettings_Type) ('Visio XML')

Indique si un paramètre d'extension d'alignement spécifique est activé ou désactivé pour la fenêtre active. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contient les éléments qui spécifient les paramètres de document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur de l'élément **SnapExtensions** peut être une somme des valeurs indiquées dans le tableau suivant. 
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|0,1  <br/> |Ancrer à l'extension du rectangle de sélection.  <br/> |
|n°2  <br/> |Extension de l'axe aligner sur le centre.  <br/> |
|4  <br/> |Magnétisme de l'extension tangente Curve.  <br/> |
|8bits  <br/> |Ancrer sur l'extension de point de terminaison.  <br/> |
|Seiz  <br/> |Ancrer sur l'extension de milieu.  <br/> |
|32  <br/> |Aligner sur l'extension linéaire.  <br/> |
|64  <br/> |Magnétisme de l'extension de courbe.  <br/> |
|128  <br/> |Aligner sur le point de terminaison perpendiculaire.  <br/> |
|256  <br/> |Magnétisme de l'extension perpendiculaire au milieu.  <br/> |
|512  <br/> |Aligner sur l'extension horizontale du point de terminaison.  <br/> |
|1024  <br/> |Aligner sur l'extension verticale du point de terminaison.  <br/> |
|2048  <br/> |Aligner sur le poste du centre de l'ellipse.  <br/> |
|4096  <br/> |Magnétisme de l'extension angles isométriques.  <br/> |
   

