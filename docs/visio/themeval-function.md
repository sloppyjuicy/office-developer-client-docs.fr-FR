---
title: Fonction THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Récupère les valeurs du thème actif.
ms.openlocfilehash: 7bbd017c859a0a167bbd279d60af029e98421375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789900"
---
# <a name="themeval-function"></a>Fonction THEMEVAL

Récupère les valeurs du thème actif. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013 
  
## <a name="syntax"></a>Syntaxe

 **THEMEVAL** ([ _« theme_value »_] [, _défaut_]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _« theme_value »_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Le nom d’une cellule dans la définition de thème permettant d’obtenir une valeur.  <br/> |
| _default_ <br/> |Facultatif  <br/> |Divers  <br/> |Une valeur par défaut si le document n’est pas à thème (il n’existe aucune définition de thème).  <br/> |
   
## <a name="remarks"></a>Remarques

Si la fonction **THEMEVAL** ne reçoit pas d’arguments, elle renvoie la valeur de la cellule hôte à thème. Il s’agit de la valeur stockée dans la définition du thème actif. La cellule hôte doit être capable d’à thème pour renvoyer une valeur ; Si la cellule n’est pas susceptibles d’être à thème, **THEMEVAL** renvoie une erreur. 
  
Si la fonction **THEMEVAL** reçoit un argument unique, il récupère la valeur de la définition du thème passée en tant qu’argument. L’argument passé pour le premier paramètre doit être un entier ou une chaîne exacte répertoriés dans le tableau ci-dessous. 
  
La fonction **THEMEVAL** peut également accepter un entier pour le premier paramètre, une valeur comprise entre 1 et 8. À l’aide des valeurs de type integer récupère une couleur par index dans le jeu de couleurs du thème. Par conséquent, une valeur de '1' renverra « foncé » du thème, « 2 » renvoie la couleur « Clair », « 3 » renvoie la couleur « Accent 1 », etc.. 
  
Si la fonction **THEMEVAL** reçoit deux arguments, elle récupère la valeur de la définition de thème transmise comme premier argument. Toutefois, si le document a aucun thème appliqué, la fonction **THEMEVAL** utilise la valeur spécifiée comme second argument. 
  
**Arguments possibles pour le paramètre « theme_value »**

|**Valeur**|**Description**|
|:-----|:-----|
|« Foncé »  <br/> |Récupère la couleur RVB foncé de la définition de thème.  <br/> |
|« Clair »  <br/> |Récupère la couleur RVB clair à partir de la définition de thème.  <br/> |
|« BackgroundColor »  <br/> |Récupère la couleur RVB d’arrière-plan de la définition de thème.  <br/> |
|« AccentColor »  <br/> |Récupère la couleur RVB Accent1 à partir de la définition de thème.  <br/> |
|« AccentColor2 »  <br/> |Récupère la couleur RVB Accent2 à partir de la définition de thème.  <br/> |
|« AccentColor3 »  <br/> |Récupère la couleur RVB Accent3 à partir de la définition de thème.  <br/> |
|« AccentColor4 »  <br/> |Récupère la couleur RVB Accent4 à partir de la définition de thème.  <br/> |
|« AccentColor5 »  <br/> |Récupère la couleur RVB Accent5 à partir de la définition de thème.  <br/> |
|« AccentColor6 »  <br/> |Récupère la couleur RVB Accent6 à partir de la définition de thème.  <br/> |
|« LinePattern »  <br/> |Récupère la valeur de la cellule LinePattern à partir de la définition de thème.  <br/> |
|« LineWeight »  <br/> |Récupère la valeur de la cellule LineWeight à partir de la définition de thème.  <br/> |
|« LineColor »  <br/> |Récupère la valeur de la cellule LineColor à partir de la définition de thème.  <br/> |
|« LineCap »  <br/> |Récupère la valeur de la cellule LineCap à partir de la définition de thème.  <br/> |
|« LineBegin »  <br/> |Récupère la valeur de la cellule BeginArrow à partir de la définition de thème.  <br/> |
|« LineEnd »  <br/> |Récupère la valeur de la cellule EndArrow à partir de la définition de thème.  <br/> |
|« LineColorTrans »  <br/> |Récupère la valeur de la cellule LineColorTrans à partir de la définition de thème.  <br/> |
|« LineCompoundtype »  <br/> |Récupère la valeur de la cellule CompoundType de la définition de thème.  <br/> |
|« LineBegin »  <br/> |Récupère la valeur de la cellule BeginArrow à partir de la définition de thème.  <br/> |
|« LineEnd »  <br/> |Récupère la valeur de la cellule EndArrow à partir de la définition de thème.  <br/> |
|« LineBeginSize »  <br/> |Récupère la valeur de la cellule BeginArrowSize à partir de la définition de thème.  <br/> |
|« LineEndSize »  <br/> |Récupère la valeur de la cellule EndArrowSize à partir de la définition de thème.  <br/> |
|« LineRounding »  <br/> |Récupère la valeur de la cellule Rounding à partir de la définition de thème.  <br/> |
|« ConnectorColor »  <br/> |Récupère la valeur de la cellule LineColor à partir de la définition de thème.  <br/> |
|« ConnectorPattern »  <br/> |Récupère la valeur de la cellule LinePattern à partir de la définition de thème.  <br/> |
|« ConnectorWeight »  <br/> |Récupère la valeur de la cellule LineWeight à partir de la définition de thème.  <br/> |
|« ConnectorTransparency »  <br/> |Récupère la valeur de la cellule LineColorTrans à partir de la définition de thème.  <br/> |
|« ConnectorRounding »  <br/> |Récupère la valeur de la cellule Rounding à partir de la définition de thème.  <br/> |
|« ConnectorBegin »  <br/> |Récupère la valeur de la cellule BeginArrow à partir de la définition de thème.  <br/> |
|Paramètre « ConnectorEnd »  <br/> |Récupère la valeur de la cellule EndArrow à partir de la définition de thème.  <br/> |
|« ConnectorBeginSize »  <br/> |Récupère la valeur de la cellule BeginArrowSize à partir de la définition de thème.  <br/> |
|« ConnectorEndSize »  <br/> |Récupère la valeur de la cellule EndArrowSize à partir de la définition de thème.  <br/> |
|« FillColor »  <br/> |Récupère la valeur de la cellule FillForegnd à partir de la définition de thème.  <br/> |
|« FillColor2 »  <br/> |Récupère la valeur de la cellule FillBkgnd à partir de la définition de thème.  <br/> |
|« FillTransparency »  <br/> |Récupère la valeur de la cellule FillForegndTrans à partir de la définition de thème.  <br/> |
|« FillPattern »  <br/> |Récupère la valeur de la cellule FillPattern à partir de la définition de thème.  <br/> |
|« LineGradientEnabled »  <br/> |Récupère la valeur de la cellule LineGradientEnabled de la définition de thème.  <br/> |
|« LineGradientDir »  <br/> |Récupère la valeur de la cellule LineGradientDir de la définition de thème.  <br/> |
|« LineGradientAngle »  <br/> |Récupère la valeur de la cellule LineGradientAngle de la définition de thème.  <br/> |
|« FillGradientEnabled »  <br/> |Récupère la valeur de la cellule FillGradientEnabled de la définition de thème.  <br/> |
|« FillGradientDir »  <br/> |Récupère la valeur de la cellule FillGradientDir de la définition de thème.  <br/> |
|« FillGradientAngle »  <br/> |Récupère la valeur de la cellule FillGradientAngle de la définition de thème.  <br/> |
|« RotateGradientWithShape »  <br/> |Récupère la valeur de la cellule RotateGradientWithShape de la définition de thème.  <br/> |
|« UseGroupGradient »  <br/> |Récupère la valeur de la cellule UseGroupGradient de la définition de thème.  <br/> |
|« ShadowType »  <br/> |Récupère la valeur de la cellule ShapeShdwType à partir de la définition de thème.  <br/> |
|« ShadowColor »  <br/> |Récupère la valeur de la cellule ShdwColor de la définition de thème.  <br/> |
|« ShadowTransparency »  <br/> |Récupère la valeur de la cellule ShdwColorTrans de la définition de thème.  <br/> |
|« ShadowMagnification »  <br/> |Récupère la valeur de la cellule ShapeShdwScaleFactor à partir de la définition de thème.  <br/> |
|« ShadowBlur »  <br/> |Récupère la valeur de la cellule ShapeShdwBlur de la définition de thème.  <br/> |
|« ShadowXOffset »  <br/> |Récupère la valeur de la cellule ShapeShdwOffsetX à partir de la définition de thème.  <br/> |
|« ShadowYOffset »  <br/> |Récupère la valeur de la cellule ShapeShdwOffsetY à partir de la définition de thème.  <br/> |
|« ShadowDirection »  <br/> |Récupère la valeur de la cellule ShapeShdwObliqueAngle à partir de la définition de thème.  <br/> |
|« ShadowPattern »  <br/> |Récupère la valeur de la cellule ShdwPattern à partir de la définition de thème.  <br/> |
|« BevelTopType »  <br/> |Récupère la valeur de la cellule BevelTopType à partir de la définition de thème.  <br/> |
|« BevelTopWidth »  <br/> |Récupère la valeur de la cellule BevelTopWidth de la définition de thème.  <br/> |
|« BevelTopHeight »  <br/> |Récupère la valeur de la cellule BevelTopHeight de la définition de thème.  <br/> |
|« BevelMaterial »  <br/> |Récupère la valeur de la cellule BevelMaterialType de la définition de thème.  <br/> |
|« BevelLighting »  <br/> |Récupère la valeur de la cellule BevelLightingType de la définition de thème.  <br/> |
|« BevelLightingAngle »  <br/> |Récupère la valeur de la cellule BevelLightingAngle de la définition de thème.  <br/> |
|« BevelContourColor »  <br/> |Récupère la valeur de la cellule BevelContourColor de la définition de thème.  <br/> |
|« BevelContourSize »  <br/> |Récupère la valeur de la cellule BevelContourSize de la définition de thème.  <br/> |
|« ReflectionBlur »  <br/> |Récupère la valeur de la cellule ReflectionBlur de la définition de thème.  <br/> |
|« ReflectionDist »  <br/> |Récupère la valeur de la cellule ReflectionDist de la définition de thème.  <br/> |
|« ReflectionSize »  <br/> |Récupère la valeur de la cellule ReflectionSize de la définition de thème.  <br/> |
|« ReflectionTrans »  <br/> |Récupère la valeur de la cellule ReflectionTrans de la définition de thème.  <br/> |
|« SoftEdgesSize »  <br/> |Récupère la valeur de la cellule SoftEdgesSize de la définition de thème.  <br/> |
|« GlowSize »  <br/> |Récupère la valeur de la cellule GlowSize de la définition de thème.  <br/> |
|« GlowColor »  <br/> |Récupère la valeur de la cellule GlowColor de la définition de thème.  <br/> |
|« GlowTransparency »  <br/> |Récupère la valeur de la cellule GlowColorTrans de la définition de thème.  <br/> |
|« SketchAmount »  <br/> |Récupère la valeur de la cellule SketchAmount de la définition de thème.  <br/> |
|« SketchEnabled »  <br/> |Récupère la valeur de la cellule SketchEnabled de la définition de thème.  <br/> |
|« SketchFillChange »  <br/> |Récupère la valeur de la cellule SketchFillChange de la définition de thème.  <br/> |
|« SketchLineChange »  <br/> |Récupère la valeur de la cellule SketchLineChange de la définition de thème.  <br/> |
|« SketchLineWeight »  <br/> |Récupère la valeur de la cellule SketchLineWeight de la définition de thème.  <br/> |
|« LatinFont »  <br/> |Récupère la valeur de la cellule Font de la définition de thème.  <br/> |
|« TextColor »  <br/> |Récupère la valeur de couleur de la cellule de la définition de thème.  <br/> |
|« TextStyle »  <br/> |Récupère la valeur de la cellule Character.Style à partir de la définition de thème.  <br/> |
|« ComplexFont »  <br/> |Récupère la valeur de la cellule ComplexScriptFont à partir de la définition de thème.  <br/> |
|« AsianFont »  <br/> |Récupère la valeur de la cellule AsianFont à partir de la définition de thème.  <br/> |
|« Color FillStop [x] »  <br/> |Récupère la valeur de cellule de couleur de ligne *x* de la définition de thème.  <br/> |
|« Transparence FillStop [x] »  <br/> |Récupère la valeur de cellule de ColorTrans dans la ligne *x* de la définition de thème.  <br/> |
|« Position FillStop [x] »  <br/> |Récupère la valeur de la cellule Position dans la ligne *x* de la définition de thème.  <br/> |
|« Color LineStop [x] »  <br/> |Récupère la valeur de cellule de couleur de ligne *x* de la définition de thème.  <br/> |
|« Transparence LineStop [x] »  <br/> |Récupère la valeur de cellule de ColorTrans dans la ligne *x* de la définition de thème.  <br/> |
|« Position LineStop [x] »  <br/> |Récupère la valeur de la cellule Position dans la ligne *x* de la définition de thème.  <br/> |
   
## <a name="example"></a>Exemple

 `THEMEVAL("5")`
  
Renvoie la couleur « Accent 3 » de la définition de thème.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Renvoie la valeur de la cellule « LineWeight » de la définition de thème. Si la forme qui contient cette fonction a aucun thème appliqué, la fonction renvoie « 0,7 pt. ».
  

