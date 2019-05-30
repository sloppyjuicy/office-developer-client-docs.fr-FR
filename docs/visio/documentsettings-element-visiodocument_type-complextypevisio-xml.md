---
title: Élément DocumentSettings (complexType VisioDocument_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contient les éléments qui spécifient les paramètres de document.
ms.openlocfilehash: 0d8e0809afae7b3de059166343577bb58f0eb01b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540069"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>Élément DocumentSettings (complexType VisioDocument_Type) (XML Visio)

Contient les éléments qui spécifient les paramètres de document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Fichier MIME (Multipurpose Internet Mail Extensions) encodé Microsoft Visio (VSU) représentant des barres d’outils personnalisées.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contient le nom du fichier d’interface utilisateur Microsoft Visio (. VSU) qui définit les menus et les raccourcis personnalisés d’un document.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contient le nom du fichier d’interface utilisateur Microsoft Visio (. VSU) qui définit les barres d’outils et les barres d’état personnalisées d’un document.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Indique si la fonctionnalité de grille dynamique est activée pour un document ou une fenêtre.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets vers lesquels les formes se collent lorsque le collage est activé dans le document.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Indique si l’utilisateur ne peut pas supprimer ou modifier des pages d’arrière-plan.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Indique si l’utilisateur ne peut pas créer, modifier ou supprimer des formes de réplicas. Quelle que soit la valeur de ce paramètre, l’utilisateur peut toujours créer des instances de formes de réplicas.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Indique si l’utilisateur ne peut pas sélectionner les formes dont l’élément **LockSelect** est défini sur 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Indique si l’utilisateur ne peut pas créer ou modifier des styles.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contient une collection d’éléments **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Indique si un paramètre d’extension d’alignement spécifique est activé ou désactivé pour la fenêtre active.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets sur lesquels aligner les formes lorsque l’alignement est actif dans la fenêtre.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément **StyleSheet** .  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément **StyleSheet** .  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément **StyleSheet** .  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément **StyleSheet** .  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Page de la page  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la page qui doit être affichée lorsque le document est ouvert par Microsoft Visio.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

