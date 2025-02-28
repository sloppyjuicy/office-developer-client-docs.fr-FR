---
title: Élément Window (Windows_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Représente une fenêtre ouverte dans une instance de Microsoft Visio. Cet élément contient les informations nécessaires à la re-création d’une fenêtre d’interface utilisateur dans l’espace de travail de l’application lorsque le fichier est initialement ouvert par Visio.
ms.openlocfilehash: 8d9c90a86a73ba121184389625816da966c3cc54
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522512"
---
# <a name="window-element-windows_type-complextype-visio-xml"></a>Élément Window (Windows_Type complexType) (Visio XML)

Représente une fenêtre ouverte dans une instance de Microsoft Visio. Cet élément contient les informations nécessaires à la re-création d’une fenêtre d’interface utilisateur dans l’espace de travail de l’application lorsque le fichier est initialement ouvert par Visio.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Fenêtres](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contient les **éléments Window** d’un document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Spécifie si la fonctionnalité de grille dynamique est activée pour un document ou une fenêtre. |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets sur qui les formes collent lorsque le collage est activé dans le document. |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Spécifie si les points de connexion sont affichés dans une fenêtre. |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Spécifie si une grille est affichée dans la fenêtre de dessin. |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Spécifie si les repères sont affichés dans la fenêtre de dessin. |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Spécifie si les coupures de page sont affichées dans une fenêtre. |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Spécifie si les règles sont affichées dans la fenêtre de dessin. |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contient une collection **d’éléments SnapAngle** . |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Spécifie si un paramètre d’extension d’snap spécifique est activé ou désactivé pour la fenêtre active. |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets sur qui les formes s’ancrent lorsque l’a snap est actif dans la fenêtre. |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Spécifie le groupe de fenêtres de gabarit fusionnées dont la fenêtre est membre. |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contient un nombre integer qui spécifie la position relative d’un gabarit au sein d’un groupe dans une fenêtre. |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Spécifie la largeur du contrôle d’onglet de page d’une fenêtre de dessin (en tant que fraction de la largeur totale de la fenêtre de dessin). |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Conteneur  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID du conteneur : Page, Feuille ou Maître. Pertinent et nécessaire uniquement si **ContainerType** est spécifié. |Valeurs du type xsd:unsignedInt. |
|ContainerType  <br/> |xsd:token  <br/> |facultatif  <br/> |Peut être l’une des valeurs suivantes : Document, Page ou Master. Pertinent uniquement **lorsque WindowType** est spécifié en tant que Dessin ou Feuille. |Valeurs du type xsd:token. |
|Document  <br/> |xsd:string  <br/> |facultatif  <br/> |Chemin d’accès au fichier du document affiché dans cette fenêtre. |Valeurs du type xsd:string. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent. |Valeurs du type xsd:unsignedInt. |
|Master  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID maître si cette fenêtre affiche une master. |Valeurs du type xsd:unsignedInt. |
|Page  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de page si cette fenêtre affiche une page. Pertinent uniquement **lorsque WindowType** est spécifié en tant que Drawing et **ContainerType** est spécifié en tant que Page. |Valeurs du type xsd:unsignedInt. |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de la fenêtre dans laquelle se trouve cette fenêtre de gabarit. Pertinent uniquement **lorsque WindowType** est spécifié en tant que Gabarit. |Valeurs du type xsd:unsignedInt. |
|ReadOnly  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indicateur en lecture seule si ce gabarit n’est pas un gabarit de document. |Valeurs du type xsd:boolean. |
|Sheet  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de la feuille dans le conteneur. Pertinent uniquement lorsque le conteneur est spécifié en tant que feuille. |Valeurs du type xsd:unsignedInt. |
|ViewCenterX  <br/> |xsd:double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’une nouvelle vue (fenêtre) suppose lorsqu’elle est ouverte initialement. |Valeurs du type xsd:double. |
|ViewCenterY  <br/> |xsd:double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’une nouvelle vue (fenêtre) suppose lorsqu’elle est ouverte initialement. |Valeurs du type xsd:double. |
|ViewScale  <br/> |xsd:double  <br/> |facultatif  <br/> |Facteur de grossissement par défaut à utiliser lors de l’ouverture d’un nouvel affichage (fenêtre) de la page. Par exemple, 1 = 100 %; 1,5 = 150 %, etc. |Valeurs du type xsd:double. |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Hauteur du rectangle de la fenêtre. |Valeurs du type xsd:unsignedInt. |
|WindowLeft  <br/> |xsd:short  <br/> |facultatif  <br/> |Coordonnée gauche du rectangle de la fenêtre. |Valeurs du type xsd:short. |
|WindowState  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Nombre nombre nombre nombre spécifiant des indicateurs de bits. |Valeurs du type xsd:unsignedInt. |
|WindowTop  <br/> |xsd:short  <br/> |facultatif  <br/> |Coordonnée supérieure du rectangle de la fenêtre. |Valeurs du type xsd:short. |
|WindowType  <br/> |xsd:token  <br/> |obligatoire  <br/> |Valeur éumée qui peut être l’une des valeurs suivantes : Dessin, Feuille, Gabarit ou Icône. |Valeurs du type xsd:token. |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Largeur du rectangle de la fenêtre. |Valeurs du type xsd:unsignedInt. |
   

