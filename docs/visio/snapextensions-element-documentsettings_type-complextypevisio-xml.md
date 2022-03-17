---
title: Élément SnapExtensions (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active.
ms.openlocfilehash: b187b8073dfb501579fcd7ff9f95c8fd3e658cb5
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521337"
---
# <a name="snapextensions-element-documentsettings_type-complextype-visio-xml"></a>Élément SnapExtensions (DocumentSettings_Type complexType) (Visio XML)

Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. 
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contient des éléments qui spécifient les paramètres de document. |
   
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
   

