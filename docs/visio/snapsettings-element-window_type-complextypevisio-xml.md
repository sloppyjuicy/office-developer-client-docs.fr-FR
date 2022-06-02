---
title: Élément SnapSettings (Window_Type complexType) (Visio XML)
description: L’élément SnapSettings (Window_Type complexType) (Visio XML) spécifie les objets auxquels les formes s’alignent lorsque l’alignement est actif dans la fenêtre.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
ms.openlocfilehash: 71c7f3b537be259801aff4c189d35fb9730e7a1b
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852984"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a>Élément SnapSettings (Window_Type complexType) (Visio XML)

Spécifie les objets auxquels les formes s’alignent lorsque l’alignement est actif dans la fenêtre.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
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
|1  <br/> |Ancrer aux subdivisions de règle. |
|2  <br/> |Ancrer à la grille. |
|4  <br/> |Aligne sur les repères. |
|8   <br/> |Aligne sur les poignées de sélection. |
|16  <br/> |Aligne sur les sommets. |
|32  <br/> |Aligne sur les points de connexion. |
|256  <br/> |Ancrer aux bords visibles des formes. |
|512  <br/> |Ancrer à la zone d’alignement. |
|1024  <br/> |Aligne sur les options d'extension de forme. |
|32768  <br/> |Ancrer désactivé. |
|65536  <br/> |Aligner sur les intersections. |
   

