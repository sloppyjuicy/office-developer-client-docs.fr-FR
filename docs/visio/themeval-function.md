---
title: Fonction THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Récupère les valeurs du thème actif.
ms.openlocfilehash: ba95b8a920174ee44c0349d7227258d3ee8a843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415753"
---
# <a name="themeval-function"></a>Fonction THEMEVAL

Récupère les valeurs du thème actif. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **THEMEVAL**([ _« theme_value »_][, _par défaut_]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _« theme_value »_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Nom d’une cellule de la définition de thème à partir de la valeur à partir de.  <br/> |
| _default_ <br/> |Facultatif  <br/> |Divers  <br/> |Valeur par défaut si le document n’est pas à thème (il n’existe aucune définition de thème).  <br/> |
   
## <a name="remarks"></a>Remarques

Si la **fonction THEMEVAL ne** reçoit aucun argument, elle renvoie la valeur à thème de la cellule hôte. Il s’agit de la valeur stockée dans la définition du thème actuel. La cellule hôte doit être capable d’être sur le themed pour renvoyer une valeur ; si la cellule n’est pas capable d’être à thème, **THEMEVAL** renvoie une erreur. 
  
Si la **fonction THEMEVAL** reçoit un seul argument, elle extrait la valeur de la définition de thème transmise en tant qu’argument. L’argument passé pour le premier paramètre doit être un nombre integer ou l’une des chaînes exactes répertoriées dans le tableau ci-dessous. 
  
La **fonction THEMEVAL** peut également accepter un integer pour le premier paramètre, sous la mesure d’une valeur entre 1 et 8. L’utilisation de valeurs de nombres integer extrait une couleur à l’aide d’un index à partir du modèle de couleurs du thème. Par conséquent, une valeur de « 1 » renvoie la couleur « Foncé » à partir du thème, « 2 » renvoie la couleur « Light », « 3 » renvoie la couleur « Accent 1 », etc. 
  
Si la **fonction THEMEVAL** reçoit deux arguments, elle récupère la valeur de la définition de thème transmise en tant que premier argument. Toutefois, si aucun thème n’est appliqué au document, la **fonction THEMEVAL** utilise la valeur spécifiée comme deuxième argument. 
  
**Arguments possibles pour le paramètre « theme_value »**

|**Valeur**|**Description**|
|:-----|:-----|
|« Sombre »  <br/> |Extrait la couleur RVB foncée de la définition de thème.  <br/> |
|« Light »  <br/> |Extrait la couleur RVB claire de la définition de thème.  <br/> |
|« BackgroundColor »  <br/> |Extrait la couleur RVB d’arrière-plan de la définition de thème.  <br/> |
|« AccentColor »  <br/> |Extrait la couleur RVB Accent1 de la définition de thème.  <br/> |
|« AccentColor2 »  <br/> |Extrait la couleur RVB Accent2 de la définition de thème.  <br/> |
|« AccentColor3 »  <br/> |Extrait la couleur RVB Accent3 de la définition de thème.  <br/> |
|« AccentColor4 »  <br/> |Extrait la couleur RVB Accent4 de la définition de thème.  <br/> |
|« AccentColor5 »  <br/> |Extrait la couleur RVB Accent5 de la définition de thème.  <br/> |
|« AccentColor6 »  <br/> |Extrait la couleur RVB Accent6 de la définition de thème.  <br/> |
|« LinePattern »  <br/> |Extrait la valeur de cellule LinePattern de la définition de thème.  <br/> |
|« LineWeight »  <br/> |Extrait la valeur de cellule LineWeight de la définition de thème.  <br/> |
|« LineColor »  <br/> |Extrait la valeur de cellule LineColor de la définition de thème.  <br/> |
|« LineCap »  <br/> |Extrait la valeur de cellule LineCap de la définition de thème.  <br/> |
|« LineBegin »  <br/> |Extrait la valeur de cellule BeginArrow de la définition de thème.  <br/> |
|« LineEnd »  <br/> |Extrait la valeur de cellule EndArrow de la définition de thème.  <br/> |
|« LineColorTrans »  <br/> |Extrait la valeur de cellule LineColorTrans de la définition de thème.  <br/> |
|« LineCompoundtype »  <br/> |Extrait la valeur de cellule CompoundType de la définition de thème.  <br/> |
|« LineBegin »  <br/> |Extrait la valeur de cellule BeginArrow de la définition de thème.  <br/> |
|« LineEnd »  <br/> |Extrait la valeur de cellule EndArrow de la définition de thème.  <br/> |
|« LineBeginSize »  <br/> |Extrait la valeur de cellule BeginArrowSize de la définition de thème.  <br/> |
|« LineEndSize »  <br/> |Extrait la valeur de cellule EndArrowSize de la définition de thème.  <br/> |
|« LineRounding »  <br/> |Extrait la valeur de cellule Rounding de la définition de thème.  <br/> |
|« ConnectorColor »  <br/> |Extrait la valeur de cellule LineColor de la définition de thème.  <br/> |
|« ConnectorPattern »  <br/> |Extrait la valeur de cellule LinePattern de la définition de thème.  <br/> |
|« ConnectorWeight »  <br/> |Extrait la valeur de cellule LineWeight de la définition de thème.  <br/> |
|« ConnectorTransparency »  <br/> |Extrait la valeur de cellule LineColorTrans de la définition de thème.  <br/> |
|« ConnectorRounding »  <br/> |Extrait la valeur de cellule Rounding de la définition de thème.  <br/> |
|« ConnectorBegin »  <br/> |Extrait la valeur de cellule BeginArrow de la définition de thème.  <br/> |
|« ConnectorEnd »  <br/> |Extrait la valeur de cellule EndArrow de la définition de thème.  <br/> |
|« ConnectorBeginSize »  <br/> |Extrait la valeur de cellule BeginArrowSize de la définition de thème.  <br/> |
|« ConnectorEndSize »  <br/> |Extrait la valeur de cellule EndArrowSize de la définition de thème.  <br/> |
|« FillColor »  <br/> |Extrait la valeur de cellule FillForegnd de la définition de thème.  <br/> |
|« FillColor2 »  <br/> |Extrait la valeur de cellule FillBkgnd de la définition de thème.  <br/> |
|« FillTransparency »  <br/> |Extrait la valeur de cellule FillForegndTrans de la définition de thème.  <br/> |
|« FillPattern »  <br/> |Extrait la valeur de cellule FillPattern de la définition de thème.  <br/> |
|« LineGradientEnabled »  <br/> |Extrait la valeur de cellule LineGradientEnabled de la définition de thème.  <br/> |
|« LineGradientDir »  <br/> |Extrait la valeur de cellule LineGradientDir de la définition de thème.  <br/> |
|« LineGradientAngle »  <br/> |Extrait la valeur de cellule LineGradientAngle de la définition de thème.  <br/> |
|« FillGradientEnabled »  <br/> |Extrait la valeur de cellule FillGradientEnabled de la définition de thème.  <br/> |
|« FillGradientDir »  <br/> |Extrait la valeur de cellule FillGradientDir de la définition de thème.  <br/> |
|« FillGradientAngle »  <br/> |Extrait la valeur de cellule FillGradientAngle de la définition de thème.  <br/> |
|« RotateGradientWithShape »  <br/> |Extrait la valeur de cellule RotateGradientWithShape de la définition de thème.  <br/> |
|« UseGroupGradient »  <br/> |Extrait la valeur de cellule UseGroupGradient de la définition de thème.  <br/> |
|« ShadowType »  <br/> |Extrait la valeur de cellule ShapeShdwType de la définition de thème.  <br/> |
|« ShadowColor »  <br/> |Extrait la valeur de cellule ShdwColor de la définition de thème.  <br/> |
|« ShadowTransparency »  <br/> |Extrait la valeur de cellule ShdwColorTrans de la définition de thème.  <br/> |
|« ShadowMagnification »  <br/> |Extrait la valeur de cellule ShapeShdwScaleFactor de la définition de thème.  <br/> |
|« ShadowBlur »  <br/> |Extrait la valeur de cellule ShapeShdwBlur de la définition de thème.  <br/> |
|« ShadowXOffset »  <br/> |Extrait la valeur de cellule ShapeShdwOffsetX de la définition de thème.  <br/> |
|« ShadowYOffset »  <br/> |Extrait la valeur de cellule ShapeShdwOffsetY de la définition de thème.  <br/> |
|« ShadowDirection »  <br/> |Extrait la valeur de cellule ShapeShdwObliqueAngle de la définition de thème.  <br/> |
|« ShadowPattern »  <br/> |Extrait la valeur de cellule ShdwPattern de la définition de thème.  <br/> |
|« BevelTopType »  <br/> |Extrait la valeur de cellule BevelTopType de la définition de thème.  <br/> |
|« BevelTopWidth »  <br/> |Extrait la valeur de cellule BevelTopWidth de la définition de thème.  <br/> |
|« BevelTopHeight »  <br/> |Extrait la valeur de cellule BevelTopHeight de la définition de thème.  <br/> |
|« BevelMaterial »  <br/> |Extrait la valeur de cellule BevelMaterialType de la définition de thème.  <br/> |
|« BevelLighting »  <br/> |Extrait la valeur de cellule BevelLightingType de la définition de thème.  <br/> |
|« BevelLightingAngle »  <br/> |Extrait la valeur de cellule BevelLightingAngle de la définition de thème.  <br/> |
|« BevelContourColor »  <br/> |Extrait la valeur de cellule BevelContourColor de la définition de thème.  <br/> |
|« BevelContourSize »  <br/> |Extrait la valeur de cellule BevelContourSize de la définition de thème.  <br/> |
|« ReflectionBlur »  <br/> |Extrait la valeur de cellule ReflectionBlur de la définition de thème.  <br/> |
|« ReflectionDist »  <br/> |Extrait la valeur de cellule ReflectionDist de la définition de thème.  <br/> |
|« ReflectionSize »  <br/> |Extrait la valeur de cellule ReflectionSize de la définition de thème.  <br/> |
|« ReflectionTrans »  <br/> |Extrait la valeur de cellule ReflectionTrans de la définition de thème.  <br/> |
|« SoftEdgesSize »  <br/> |Extrait la valeur de cellule SoftEdgesSize de la définition de thème.  <br/> |
|« GlowSize »  <br/> |Extrait la valeur de cellule GlowSize de la définition de thème.  <br/> |
|« GlowColor »  <br/> |Extrait la valeur de cellule GlowColor de la définition de thème.  <br/> |
|« GlowTransparency »  <br/> |Extrait la valeur de cellule GlowColorTrans de la définition de thème.  <br/> |
|« SketchAmount »  <br/> |Extrait la valeur de cellule SketchAmount de la définition de thème.  <br/> |
|« SketchEnabled »  <br/> |Extrait la valeur de cellule SketchEnabled de la définition de thème.  <br/> |
|« SketchFillChange »  <br/> |Extrait la valeur de cellule SketchFillChange de la définition de thème.  <br/> |
|« SketchLineChange »  <br/> |Extrait la valeur de cellule SketchLineChange de la définition de thème.  <br/> |
|« SketchLineWeight »  <br/> |Extrait la valeur de cellule SketchLineWeight de la définition de thème.  <br/> |
|« LatinFont »  <br/> |Extrait la valeur de cellule Font de la définition de thème.  <br/> |
|« TextColor »  <br/> |Extrait la valeur de cellule Color de la définition de thème.  <br/> |
|« TextStyle »  <br/> |Extrait la valeur de cellule Character.Style de la définition de thème.  <br/> |
|« ComplexFont »  <br/> |Extrait la valeur de cellule ComplexScriptFont de la définition de thème.  <br/> |
|« AsianFont »  <br/> |Extrait la valeur de cellule AsianFont de la définition de thème.  <br/> |
|« FillStop[x]Color »  <br/> |Extrait la valeur de cellule Color de la ligne  *x*  à partir de la définition de thème.  <br/> |
|« FillStop[x]Transparency »  <br/> |Extrait la valeur de cellule ColorTrans de la ligne  *x*  à partir de la définition de thème.  <br/> |
|« FillStop[x]Position »  <br/> |Extrait la valeur de cellule Position de la ligne  *x*  à partir de la définition de thème.  <br/> |
|« LineStop[x]Color »  <br/> |Extrait la valeur de cellule Color de la ligne  *x*  à partir de la définition de thème.  <br/> |
|« LineStop[x]Transparency »  <br/> |Extrait la valeur de cellule ColorTrans de la ligne  *x*  à partir de la définition de thème.  <br/> |
|« LineStop[x]Position »  <br/> |Extrait la valeur de cellule Position de la ligne  *x*  à partir de la définition de thème.  <br/> |
   
## <a name="example"></a>Exemple

 `THEMEVAL("5")`
  
Renvoie la couleur « Accent 3 » à partir de la définition de thème.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Renvoie la valeur de la cellule « LineWeight » à partir de la définition de thème. Si aucun thème n’est appliqué à la forme contenant cette fonction, la fonction renvoie « 0,7 pt ».
  

