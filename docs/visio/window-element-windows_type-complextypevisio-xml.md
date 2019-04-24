---
title: Window, élément (Windows_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Représente une fenêtre ouverte dans une instance de Microsoft Visio. Cet élément contient les informations nécessaires à la recréation d'une fenêtre d'interface utilisateur dans l'espace de travail d'application lors de l'ouverture initiale du fichier par Visio.
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339899"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Window, élément (Windows_Type complexType) ('Visio XML')

Représente une fenêtre ouverte dans une instance de Microsoft Visio. Cet élément contient les informations nécessaires à la recréation d'une fenêtre d'interface utilisateur dans l'espace de travail d'application lors de l'ouverture initiale du fichier par Visio.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Windows. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Fenêtres](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contient les éléments **Window** d'un document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Indique si la fonctionnalité de grille dynamique est activée pour un document ou une fenêtre.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets vers lesquels les formes se collent lorsque le collage est activé dans le document.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Indique si les points de connexion sont affichés dans une fenêtre.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Indique si une grille est affichée dans la fenêtre de dessin.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Indique si les repères sont affichés dans la fenêtre de dessin.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Indique si les sauts de page sont affichés dans une fenêtre.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Indique si les règles sont affichées dans la fenêtre de dessin.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contient une collection d'éléments **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Indique si un paramètre d'extension d'alignement spécifique est activé ou désactivé pour la fenêtre active.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets sur lesquels aligner les formes lorsque l'alignement est actif dans la fenêtre.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Spécifie le groupe de fenêtres de stencil fusionné dont la fenêtre est membre.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contient un entier qui spécifie la position relative d'un gabarit dans un groupe dans une fenêtre.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie la largeur du contrôle d'onglet de page d'une fenêtre de dessin (sous la forme d'une fraction de la largeur totale de la fenêtre de dessin).  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID du conteneur: page, Sheet ou Master. Uniquement pertinent et nécessaire si **ContainerType** est spécifié.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ContainerType  <br/> |xsd: Token  <br/> |facultatif  <br/> |Peut être l'une des valeurs suivantes: document, page ou Master. S'applique uniquement lorsque **WindowType** est spécifié en tant que Drawing ou Sheet.  <br/> |Valeurs du type xsd: Token.  <br/> |
|Document  <br/> |xsd: String  <br/> |facultatif  <br/> |Chemin d'accès de fichier du document affiché dans cette fenêtre.  <br/> |Valeurs du type xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID unique de l'élément au sein de son élément parent.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Master  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID maître si cette fenêtre affiche une forme de base.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Page  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de page si cette fenêtre affiche une page. S'applique uniquement lorsque **WindowType** est spécifié en tant que Drawing et **ContainerType** est spécifié en tant que page.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ParentWindow  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de la fenêtre dans laquelle cette fenêtre de gabarit est contenue. S'applique uniquement lorsque **WindowType** est spécifié en tant que gabarit.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ReadOnly  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indicateur en lecture seule s'il ne s'agit pas d'un gabarit de document.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|Sheet  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de la feuille dans le conteneur. Pertinent uniquement lorsque le conteneur est spécifié en tant que feuille.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu'un nouvel affichage (fenêtre) présuppose lorsqu'il est ouvert au départ.  <br/> |Valeurs du type xsd: double.  <br/> |
|ViewCenterY  <br/> |xsd: double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu'un nouvel affichage (fenêtre) présuppose lorsqu'il est ouvert au départ.  <br/> |Valeurs du type xsd: double.  <br/> |
|ViewScale  <br/> |xsd: double  <br/> |facultatif  <br/> |Facteur d'agrandissement par défaut à utiliser lors de l'ouverture d'une nouvelle vue (fenêtre) de la page. Par exemple, 1 = 100%; 1,5 = 150%, etc.  <br/> |Valeurs du type xsd: double.  <br/> |
|WindowHeight  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Hauteur du rectangle de la fenêtre.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|WindowLeft  <br/> |xsd: Short  <br/> |facultatif  <br/> |Coordonnée gauche du rectangle de la fenêtre.  <br/> |Valeurs du type xsd: short.  <br/> |
|WindowState  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Entier spécifiant des indicateurs binaires.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|WindowTop  <br/> |xsd: Short  <br/> |facultatif  <br/> |Coordonnée supérieure du rectangle de la fenêtre.  <br/> |Valeurs du type xsd: short.  <br/> |
|WindowType  <br/> |xsd: Token  <br/> |obligatoire  <br/> |Une valeur énumérée qui peut être l'une des valeurs suivantes: Drawing, Sheet, stencil ou Icon.  <br/> |Valeurs du type xsd: Token.  <br/> |
|WindowWidth  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Largeur du rectangle de la fenêtre.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
   

