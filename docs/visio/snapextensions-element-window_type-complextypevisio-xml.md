---
title: Élément SnapExtensions (complexType Window_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Indique si un paramètre d’extension d’alignement spécifique est activé ou désactivé pour la fenêtre active. La valeur peut être une somme des valeurs du tableau suivant.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540321"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>Élément SnapExtensions (complexType Window_Type) (XML Visio)

Indique si un paramètre d’extension d’alignement spécifique est activé ou désactivé pour la fenêtre active. La valeur peut être une somme des valeurs du tableau suivant.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Windows. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur de l’élément **SnapExtensions** peut être une somme des valeurs indiquées dans le tableau suivant. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|0,1  <br/> |Ancrer à l’extension du rectangle de sélection.  <br/> |
|n°2  <br/> |Extension de l’axe aligner sur le centre.  <br/> |
|4  <br/> |Magnétisme de l’extension tangente Curve.  <br/> |
|8bits  <br/> |Ancrer sur l’extension de point de terminaison.  <br/> |
|Seiz  <br/> |Ancrer sur l’extension de milieu.  <br/> |
|32  <br/> |Aligner sur l’extension linéaire.  <br/> |
|64  <br/> |Magnétisme de l’extension de courbe.  <br/> |
|128  <br/> |Aligner sur le point de terminaison perpendiculaire.  <br/> |
|256  <br/> |Magnétisme de l’extension perpendiculaire au milieu.  <br/> |
|512  <br/> |Aligner sur l’extension horizontale du point de terminaison.  <br/> |
|1024  <br/> |Aligner sur l’extension verticale du point de terminaison.  <br/> |
|2048  <br/> |Aligner sur le poste du centre de l’ellipse.  <br/> |
|4096  <br/> |Magnétisme de l’extension angles isométriques.  <br/> |
   

