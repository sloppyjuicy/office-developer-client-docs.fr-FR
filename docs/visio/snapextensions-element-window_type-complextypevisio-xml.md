---
title: Élément SnapExtensions (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. La valeur peut être une somme des valeurs du tableau suivant.
ms.openlocfilehash: 84e8888f8214db9a9b86c46a5387546a6323259b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779186"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>Élément SnapExtensions (Window_Type complexType) (Visio XML)

Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. La valeur peut être une somme des valeurs du tableau suivant.
  
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
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
|0  <br/> |Aligne sur rien. |
|1  <br/> |Aligner sur l’extension du cadre d’alignement. |
|2  <br/> |Aligner sur l’extension de l’axe central. |
|4  <br/> |Aligner pour courber l’extension tangente. |
|8   <br/> |Aligner sur l’extension de point de terminaison. |
|16  <br/> |Aligner sur l’extension de point intermédiaire. |
|32  <br/> |Aligner sur une extension linéaire. |
|64  <br/> |Aligner sur l’extension de courbe. |
|128  <br/> |Aligner sur l’extension perpendiculaire du point de terminaison. |
|256  <br/> |Aligner sur l’extension perpendiculaire du milieu. |
|512  <br/> |Aligner sur l’extension horizontale du point de terminaison. |
|1024  <br/> |Aligner sur l’extension verticale du point de terminaison. |
|2048  <br/> |Aligner sur l’extension centrale de l’ellipse. |
|4096  <br/> |Aligner sur l’extension des angles isométriques. |
   

