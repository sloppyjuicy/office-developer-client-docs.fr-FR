---
title: SnapExtensions, élément (DocumentSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Spécifie si un paramètre d’extension de composant logiciel enfichable spécifique est activé ou désactivé pour la fenêtre active.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387614"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>SnapExtensions, élément (DocumentSettings_Type, complexType) (« Visio XML »)

Spécifie si un paramètre d’extension de composant logiciel enfichable spécifique est activé ou désactivé pour la fenêtre active. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
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

Aucune.
  
## <a name="remarks"></a>Remarques

La valeur de l’élément **SnapExtensions** peut être une somme des valeurs dans le tableau suivant. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|1  <br/> |Aligner sur l’extension du rectangle de sélection.  <br/> |
|2  <br/> |Aligner sur l’extension de l’axe centre.  <br/> |
|4  <br/> |Aligner sur l’extension tangentes de courbe.  <br/> |
|8  <br/> |Aligner sur l’extension de point de terminaison.  <br/> |
|16  <br/> |Aligner sur l’extension du milieu.  <br/> |
|32  <br/> |Aligner sur l’extension linéaire.  <br/> |
|64  <br/> |Aligner sur l’extension de la courbe.  <br/> |
|128  <br/> |Aligner sur l’extension perpendiculaire du reste du point de terminaison.  <br/> |
|256  <br/> |Aligner sur l’extension perpendiculaires du milieu.  <br/> |
|512  <br/> |Aligner sur l’extension horizontale du point de terminaison.  <br/> |
|1024  <br/> |Aligner sur extension verticale du point de terminaison.  <br/> |
|2048  <br/> |Aligner sur l’extension du centre ellipse.  <br/> |
|4096  <br/> |Aligner sur l’extension d’angle isométrique.  <br/> |
   

