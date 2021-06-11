---
title: Élément SnapExtensions (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. La valeur peut être la somme des valeurs du tableau suivant.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540321"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>Élément SnapExtensions (Window_Type complexType) (Visio XML)

Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. La valeur peut être la somme des valeurs du tableau suivant.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur de **l’élément SnapExtensions** peut être la somme des valeurs du tableau suivant. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|1  <br/> |Ancrer l’extension du cadre d’alignement.  <br/> |
|2  <br/> |Ancrer l’extension de l’axe central.  <br/> |
|4   <br/> |Ancrer l’extension tangente de courbe.  <br/> |
|8   <br/> |Ancrer l’extension de point de terminaison.  <br/> |
|16   <br/> |Ancrer à l’extension midpoint.  <br/> |
|32  <br/> |Ancrer extension linéaire.  <br/> |
|64  <br/> |Ancrer extension de courbe.  <br/> |
|128  <br/> |Ancrer l’extension perpendiculaire du point de terminaison.  <br/> |
|256  <br/> |Ancrer à l’extension perpendiculaire du milieu.  <br/> |
|512  <br/> |Ancrer l’extension horizontale du point de terminaison.  <br/> |
|1024  <br/> |Ancrer l’extension verticale du point de terminaison.  <br/> |
|2048  <br/> |Ancrer à l’extension centrale de l’ellipse.  <br/> |
|4096  <br/> |Ancrer l’extension des angles isométriques.  <br/> |
   

