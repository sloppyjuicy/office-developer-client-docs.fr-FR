---
title: SnapSettings, élément (Window_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Spécifie les objets formes s’alignent lorsque l’alignement est actif dans la fenêtre.
ms.openlocfilehash: 55558301b1f85f70f723d4282b438e4883d90c25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789772"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>SnapSettings, élément (Window_Type, complexType) (« Visio XML »)

Spécifie les objets formes s’alignent lorsque l’alignement est actif dans la fenêtre.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Représente une fenêtre ouverte dans une instance de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur peut être une somme des valeurs dans le tableau suivant.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|1  <br/> |Aligner sur les graduations de la règle.  <br/> |
|2  <br/> |Aligner sur la grille.  <br/> |
|4  <br/> |Aligne sur les repères.  <br/> |
|8  <br/> |Aligne sur les poignées de sélection.  <br/> |
|16  <br/> |Aligne sur les sommets.  <br/> |
|32  <br/> |Aligne sur les points de connexion.  <br/> |
|256  <br/> |Aligner sur les côtés visibles des formes.  <br/> |
|512  <br/> |Aligne sur le rectangle de sélection.  <br/> |
|1024  <br/> |Aligne sur les options d'extension de forme.  <br/> |
|32768  <br/> |Composant logiciel enfichable désactivé.  <br/> |
|65536  <br/> |Aligne sur les intersections.  <br/> |
   

