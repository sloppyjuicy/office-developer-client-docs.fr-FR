---
title: Élément SnapSettings (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Spécifie les objets sur qui les formes s’ancrent lorsque l’a snap est actif dans la fenêtre.
ms.openlocfilehash: 70a6384a55c65ff3b25db4ab4cbd7b1d0abd8756
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520265"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a>Élément SnapSettings (Window_Type complexType) (Visio XML)

Spécifie les objets sur qui les formes s’ancrent lorsque l’a snap est actif dans la fenêtre.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Représente une fenêtre ouverte dans une instance de Microsoft Visio. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur peut être une somme des valeurs du tableau suivant.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien. |
|1  <br/> |Aligner sur les sous-sections de règle. |
|2  <br/> |Aligner sur la grille. |
|4  <br/> |Aligne sur les repères. |
|8   <br/> |Aligne sur les poignées de sélection. |
|16  <br/> |Aligne sur les sommets. |
|32  <br/> |Aligne sur les points de connexion. |
|256  <br/> |Aligner sur les bords visibles des formes. |
|512  <br/> |Aligner sur le cadre d’alignement. |
|1024  <br/> |Aligne sur les options d'extension de forme. |
|32768  <br/> |Aligner désactivé. |
|65536  <br/> |Aligner sur les intersections. |
   

