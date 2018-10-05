---
title: Élément DocumentSettings (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contient des éléments qui spécifient les paramètres de document.
ms.openlocfilehash: e86dc5a0875006cb8bd1bbaffd36037a07fd5c0f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396468"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>Élément DocumentSettings (VisioDocument_Type, complexType) (« Visio XML »)

Contient des éléments qui spécifient les paramètres de document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |L’élément racine d’un document Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |MIME (Multipurpose Internet Mail Extensions) codés fichier d’interface (VSU) utilisateur Microsoft Visio qui représente les barres d’outils personnalisées.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contient le nom du fichier (.vsu) d’interface utilisateur Microsoft Visio qui définit les menus personnalisés et des raccourcis pour un document.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contient le nom du fichier (.vsu) d’interface utilisateur Microsoft Visio qui définit les barres d’outils personnalisées et des barres d’état pour un document.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Spécifie si la fonctionnalité de grille dynamique est activée pour une fenêtre ou un document.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets formes collent aux lorsque le collage est activé dans le document.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur ne peut pas supprimer ou de modifier des pages d’arrière-plan.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur est empêché de création, modification ou la suppression des formes de base. Quel que soit ce paramètre, l’utilisateur peut toujours créer des instances de formes de base.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur est empêché de sélection de formes qui ont leur élément **LockSelect** la valeur 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Spécifie si l’utilisateur ne peut pas créer ou modifier les styles.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contient une collection d’éléments **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Spécifie si un paramètre d’extension de composant logiciel enfichable spécifique est activé ou désactivé pour la fenêtre active.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets formes s’alignent lorsque l’alignement est actif dans la fenêtre.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément de la **feuille de style** .  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément de la **feuille de style** .  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément de la **feuille de style** .  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID d’un élément de la **feuille de style** .  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|TopPage  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’ID de la page qui doit être affichée lorsque le document est ouvert par Microsoft Visio.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

