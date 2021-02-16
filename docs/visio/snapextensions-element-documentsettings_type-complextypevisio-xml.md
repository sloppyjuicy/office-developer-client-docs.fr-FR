---
title: Élément SnapExtensions (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active.
ms.openlocfilehash: 86ff7f32d6e12b2f0d7a8387d8e5b7ae9870b5fa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540377"
---
# <a name="snapextensions-element-documentsettings_type-complextype-visio-xml"></a>Élément SnapExtensions (DocumentSettings_Type complexType) (Visio XML)

Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contient des éléments qui spécifient les paramètres de document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

Aucun.
  
## <a name="remarks"></a>Remarques

La valeur de **l’élément SnapExtensions** peut être la somme des valeurs du tableau suivant. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aligne sur rien.  <br/> |
|1   <br/> |Aligner sur l’extension du cadre d’alignement.  <br/> |
|2   <br/> |Aligner sur l’extension de l’axe central.  <br/> |
|4   <br/> |Aligner pour courber l’extension tangente.  <br/> |
|8   <br/> |Aligner sur l’extension de point de terminaison.  <br/> |
|16   <br/> |Aligner sur l’extension de point intermédiaire.  <br/> |
|32  <br/> |Aligner sur une extension linéaire.  <br/> |
|64  <br/> |Aligner sur l’extension de courbe.  <br/> |
|128  <br/> |Aligner sur l’extension perpendiculaire du point de terminaison.  <br/> |
|256  <br/> |Aligner sur l’extension perpendiculaire du milieu.  <br/> |
|512  <br/> |Aligner sur l’extension horizontale du point de terminaison.  <br/> |
|1024  <br/> |Aligner sur l’extension verticale du point de terminaison.  <br/> |
|2048  <br/> |Aligner sur l’extension centrale de l’ellipse.  <br/> |
|4096  <br/> |Aligner sur l’extension des angles isométriques.  <br/> |
   

