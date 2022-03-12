---
title: Élément DocumentSettings (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contient des éléments qui spécifient les paramètres de document.
ms.openlocfilehash: 3219eb1e673a4449a1a88e7341f80db02e432dda
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448411"
---
# <a name="documentsettings-element-visiodocument_type-complextype-visio-xml"></a>Élément DocumentSettings (VisioDocument_Type complexType) (Visio XML)

Contient des éléments qui spécifient les paramètres de document.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Fichier MIME (Multipurpose Internet Mail Extensions) codé Microsoft Visio interface utilisateur (VSU) représentant des barres d’outils personnalisées. |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contient le nom du fichier d’interface utilisateur microsoft Visio (.vsu) qui définit des menus et des accélérateurs personnalisés pour un document. |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contient le nom du fichier d’interface Visio Microsoft (.vsu) qui définit les barres d’outils et barres d’état personnalisées d’un document. |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Spécifie si la fonctionnalité de grille dynamique est activée pour un document ou une fenêtre. |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets sur qui les formes collent lorsque le collage est activé dans le document. |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur est empêché de supprimer ou de modifier des pages d’arrière-plan. |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur ne peut pas créer, modifier ou supprimer des maîtres. Quel que soit ce paramètre, l’utilisateur peut toujours créer des instances de maîtres. |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur ne peut pas sélectionner les formes dont l’élément **LockSelect** est 1. |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur est empêché de créer ou de modifier des styles. |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contient une collection **d’éléments SnapAngle** . |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets sur qui les formes s’ancrent lorsque l’a snap est actif dans la fenêtre. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un **élément StyleSheet** . |Valeurs du type xsd:unsignedInt. |
|DefaultGuideStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un **élément StyleSheet** . |Valeurs du type xsd:unsignedInt. |
|DefaultLineStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un **élément StyleSheet** . |Valeurs du type xsd:unsignedInt. |
|DefaultTextStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un **élément StyleSheet** . |Valeurs du type xsd:unsignedInt. |
|TopPage  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la page qui doit être affiché lorsque le document est ouvert par Microsoft Visio. |Valeurs du type xsd:unsignedInt. |
   

