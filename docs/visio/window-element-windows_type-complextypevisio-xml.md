---
title: Élément de la fenêtre (Windows_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: >-
  Représente une fenêtre ouverte dans une instance de Microsoft Visio.
   Cet élément contient les informations nécessaires pour recréer exactement une fenêtre de l’interface utilisateur dans l’espace de travail lorsque le fichier est ouvert à l’origine par Visio.
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385346"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Élément de la fenêtre (Windows_Type, complexType) (« Visio XML »)

Représente une fenêtre ouverte dans une instance de Microsoft Visio.
 Cet élément contient les informations nécessaires pour recréer exactement une fenêtre de l’interface utilisateur dans l’espace de travail lorsque le fichier est ouvert à l’origine par Visio.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contient les éléments de la **fenêtre** d’un document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Spécifie si la fonctionnalité de grille dynamique est activée pour une fenêtre ou un document.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets formes collent aux lorsque le collage est activé dans le document.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Indique si les points de connexion sont affichés dans une fenêtre.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Spécifie si une grille est affichée dans la fenêtre de dessin.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Indique si les repères sont affichés dans la fenêtre de dessin.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Indique si les sauts de page sont affichés dans une fenêtre.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Spécifie si les règles sont affichés dans la fenêtre de dessin.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contient une collection d’éléments **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Spécifie si un paramètre d’extension de composant logiciel enfichable spécifique est activé ou désactivé pour la fenêtre active.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Spécifie les objets formes s’alignent lorsque l’alignement est actif dans la fenêtre.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Spécifie le groupe de fenêtres de gabarit fusionnée dont la fenêtre est un membre.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contient un entier qui spécifie la position relative d’un gabarit dans un groupe dans une fenêtre.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Spécifie la largeur du contrôle onglet d’une fenêtre de dessin (comme une fraction de la largeur totale de la fenêtre de dessin).  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID de conteneur : Master, Page ou feuille. Uniquement pertinentes et nécessaires si **ContainerType** est spécifié.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |XSD:Token  <br/> |facultatif  <br/> |Peut être une des valeurs suivantes : Document, Page ou Master. Uniquement en cas de **WindowType** est spécifié en tant que dessin ou de la feuille.  <br/> |Valeurs du type xsd:token.  <br/> |
|Document  <br/> |XSD : String  <br/> |facultatif  <br/> |Chemin d’accès de fichier du document affiché dans cette fenêtre.  <br/> |Valeurs du type xsd : String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément dans l’élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID de forme de base si cette fenêtre est une forme de base.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Page  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID de page si la fenêtre affiche une page. Pertinent uniquement lorsque la **propriété WindowType** est spécifié en tant que dessin et **ContainerType** est spécifié en tant que Page.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID de la fenêtre dans laquelle se trouve cette fenêtre de gabarit. Disponible uniquement lorsque le **WindowType** est spécifié en tant que gabarit.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indicateur en lecture seule si ce gabarit n’est pas un gabarit de document.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Feuille  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |ID de feuille dans le conteneur. Pertinent uniquement lorsque le conteneur est spécifié en tant que feuille.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD : double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’un nouvel affichage (fenêtre) lorsqu’il est ouvert à l’origine.  <br/> |Valeurs du type xsd : double.  <br/> |
|ViewCenterY  <br/> |XSD : double  <br/> |facultatif  <br/> |**ViewCenterX** et **ViewCenterY** spécifient un point central sur une page qu’un nouvel affichage (fenêtre) lorsqu’il est ouvert à l’origine.  <br/> |Valeurs du type xsd : double.  <br/> |
|ViewScale  <br/> |XSD : double  <br/> |facultatif  <br/> |Le facteur d’agrandissement par défaut à utiliser lors de l’ouverture d’un nouvel affichage (fenêtre) de la page. Par exemple, 1 = 100 %. 1,5 = 150 % et ainsi de suite.  <br/> |Valeurs du type xsd : double.  <br/> |
|WindowHeight  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Hauteur du rectangle de la fenêtre.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |XSD:short  <br/> |facultatif  <br/> |Coordonnée gauche du rectangle de la fenêtre.  <br/> |Valeurs du type xsd:short.  <br/> |
|WindowState  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Un entier spécifiant bits indicateurs.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |XSD:short  <br/> |facultatif  <br/> |Coordonnée supérieure du rectangle de la fenêtre.  <br/> |Valeurs du type xsd:short.  <br/> |
|Propriété WindowType  <br/> |XSD:Token  <br/> |obligatoire  <br/> |Valeur énumérée qui peut être une des opérations suivantes : dessin, feuille, gabarit ou icône.  <br/> |Valeurs du type xsd:token.  <br/> |
|WindowWidth  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Largeur du rectangle de la fenêtre.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

