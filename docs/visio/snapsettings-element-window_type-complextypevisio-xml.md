---
title: Élément SnapSettings (Window_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Spécifie les objets sur lesquels aligner les formes lorsque l'alignement est actif dans la fenêtre.
ms.openlocfilehash: b4793c6d9c13a922db4d3ed9504a3a08e933230a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334502"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>Élément SnapSettings (Window_Type complexType) ('Visio XML')

Spécifie les objets sur lesquels aligner les formes lorsque l'alignement est actif dans la fenêtre.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Windows. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Représente une fenêtre ouverte dans une instance de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur peut être une somme des valeurs indiquées dans le tableau suivant.
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|0,1  <br/> |Aligner sur les graduations de la règle.  <br/> |
|n°2  <br/> |Aligner sur la grille.  <br/> |
|4  <br/> |Aligne sur les repères.  <br/> |
|8bits  <br/> |Aligne sur les poignées de sélection.  <br/> |
|Seiz  <br/> |Aligne sur les sommets.  <br/> |
|32  <br/> |Aligne sur les points de connexion.  <br/> |
|256  <br/> |Aligner sur les bords visibles des formes.  <br/> |
|512  <br/> |Aligner sur le rectangle de sélection.  <br/> |
|1024  <br/> |Aligne sur les options d'extension de forme.  <br/> |
|32768  <br/> |Alignement désactivé.  <br/> |
|65536  <br/> |Aligner sur les intersections.  <br/> |
   

