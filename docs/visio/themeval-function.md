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

 **THEMEVAL** ([ _"theme_value"_] [, _default_]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _«theme_value»_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Nom d'une cellule dans la définition de thème à partir de laquelle obtenir une valeur.  <br/> |
| _default_ <br/> |Facultatif  <br/> |Divers  <br/> |Valeur par défaut si le document n'est pas à thème (il n'y a pas de définition de thème).  <br/> |
   
## <a name="remarks"></a>Remarques

Si la fonction **THEMEVAL** ne reçoit pas d'argument, elle renvoie la valeur à thème de la cellule hôte. Il s'agit de la valeur stockée dans la définition du thème actuel. La cellule hôte doit pouvoir être déplacée pour renvoyer une valeur; Si la cellule ne peut pas être liée, **THEMEVAL** renvoie une erreur. 
  
Si la fonction **THEMEVAL** reçoit un seul argument, elle récupère la valeur à partir de la définition de thème transmise en tant qu'argument. L'argument transmis pour le premier paramètre doit être un entier ou une des chaînes exactes indiquées dans le tableau ci-dessous. 
  
La fonction **THEMEVAL** peut également accepter un entier pour le premier paramètre, sous la forme d'une valeur comprise entre 1 et 8. Utilisation de valeurs entières récupère une couleur à l'aide d'un index à partir du jeu de couleurs du thème. Par conséquent, la valeur «1» renvoie la couleur «sombre» à partir du thème, «2» renvoie la couleur «clair», «3» renvoie la couleur «accent 1», etc. 
  
Si la fonction **THEMEVAL** reçoit deux arguments, elle récupère la valeur à partir de la définition de thème transmise en tant que premier argument. Toutefois, si aucun thème n'est appliqué au document, la fonction **THEMEVAL** utilise la valeur spécifiée comme deuxième argument. 
  
**Arguments possibles pour le paramètre «theme_value»**

|**Valeur**|**Description**|
|:-----|:-----|
|Obscurci  <br/> |Récupère la couleur RVB foncé de la définition du thème.  <br/> |
|Activ  <br/> |Récupère la couleur lumière RVB de la définition de thème.  <br/> |
|BackgroundColor  <br/> |Récupère la couleur d'arrière-plan RVB de la définition de thème.  <br/> |
|«AccentColor»  <br/> |Récupère la couleur RVB Accent1 à partir de la définition de thème.  <br/> |
|«AccentColor2»  <br/> |Récupère la couleur RVB Accent2 à partir de la définition de thème.  <br/> |
|«AccentColor3»  <br/> |Récupère la couleur RVB Accent3 à partir de la définition de thème.  <br/> |
|«AccentColor4»  <br/> |Récupère la couleur RVB Accent4 à partir de la définition de thème.  <br/> |
|«AccentColor5»  <br/> |Récupère la couleur RVB Accent5 à partir de la définition de thème.  <br/> |
|«AccentColor6»  <br/> |Récupère la couleur RVB Accent6 à partir de la définition de thème.  <br/> |
|LinePattern  <br/> |Récupère la valeur de la cellule LinePattern à partir de la définition du thème.  <br/> |
|LineWeight  <br/> |Récupère la valeur de la cellule LineWeight à partir de la définition de thème.  <br/> |
|LineColor  <br/> |Récupère la valeur de la cellule LineColor à partir de la définition de thème.  <br/> |
|LineCap  <br/> |Récupère la valeur de la cellule LineCap à partir de la définition du thème.  <br/> |
|«LineBegin»  <br/> |Récupère la valeur de la cellule BeginArrow à partir de la définition du thème.  <br/> |
|«LineEnd»  <br/> |Récupère la valeur de la cellule EndArrow à partir de la définition de thème.  <br/> |
|LineColorTrans  <br/> |Récupère la valeur de la cellule LineColorTrans à partir de la définition du thème.  <br/> |
|«LineCompoundtype»  <br/> |Récupère la valeur de la cellule CompoundType à partir de la définition de thème.  <br/> |
|«LineBegin»  <br/> |Récupère la valeur de la cellule BeginArrow à partir de la définition du thème.  <br/> |
|«LineEnd»  <br/> |Récupère la valeur de la cellule EndArrow à partir de la définition de thème.  <br/> |
|«LineBeginSize»  <br/> |Récupère la valeur de la cellule BeginArrowSize à partir de la définition de thème.  <br/> |
|«LineEndSize»  <br/> |Récupère la valeur de la cellule EndArrowSize à partir de la définition du thème.  <br/> |
|«LineRounding»  <br/> |Récupère la valeur de la cellule d'arrondi à partir de la définition de thème.  <br/> |
|«ConnectorColor»  <br/> |Récupère la valeur de la cellule LineColor à partir de la définition de thème.  <br/> |
|«ConnectorPattern»  <br/> |Récupère la valeur de la cellule LinePattern à partir de la définition du thème.  <br/> |
|«ConnectorWeight»  <br/> |Récupère la valeur de la cellule LineWeight à partir de la définition de thème.  <br/> |
|«ConnectorTransparency»  <br/> |Récupère la valeur de la cellule LineColorTrans à partir de la définition du thème.  <br/> |
|«ConnectorRounding»  <br/> |Récupère la valeur de la cellule d'arrondi à partir de la définition de thème.  <br/> |
|«ConnectorBegin»  <br/> |Récupère la valeur de la cellule BeginArrow à partir de la définition du thème.  <br/> |
|«ConnectorEnd»  <br/> |Récupère la valeur de la cellule EndArrow à partir de la définition de thème.  <br/> |
|«ConnectorBeginSize»  <br/> |Récupère la valeur de la cellule BeginArrowSize à partir de la définition de thème.  <br/> |
|«ConnectorEndSize»  <br/> |Récupère la valeur de la cellule EndArrowSize à partir de la définition du thème.  <br/> |
|FillColor  <br/> |Récupère la valeur de la cellule FillForegnd à partir de la définition de thème.  <br/> |
|«FillColor2»  <br/> |Récupère la valeur de la cellule FillBkgnd à partir de la définition du thème.  <br/> |
|«FillTransparency»  <br/> |Récupère la valeur de la cellule FillForegndTrans à partir de la définition du thème.  <br/> |
|FillPattern  <br/> |Récupère la valeur de la cellule FillPattern à partir de la définition de thème.  <br/> |
|LineGradientEnabled  <br/> |Récupère la valeur de la cellule LineGradientEnabled à partir de la définition de thème.  <br/> |
|LineGradientDir  <br/> |Récupère la valeur de la cellule LineGradientDir à partir de la définition de thème.  <br/> |
|LineGradientAngle  <br/> |Récupère la valeur de la cellule LineGradientAngle à partir de la définition de thème.  <br/> |
|FillGradientEnabled  <br/> |Récupère la valeur de la cellule FillGradientEnabled à partir de la définition de thème.  <br/> |
|FillGradientDir  <br/> |Récupère la valeur de la cellule FillGradientDir à partir de la définition de thème.  <br/> |
|FillGradientAngle  <br/> |Récupère la valeur de la cellule FillGradientAngle à partir de la définition de thème.  <br/> |
|RotateGradientWithShape  <br/> |Récupère la valeur de la cellule RotateGradientWithShape à partir de la définition de thème.  <br/> |
|UseGroupGradient  <br/> |Récupère la valeur de la cellule UseGroupGradient à partir de la définition de thème.  <br/> |
|«ShadowType»  <br/> |Récupère la valeur de la cellule ShapeShdwType à partir de la définition de thème.  <br/> |
|«ShadowColor»  <br/> |Récupère la valeur de la cellule ShdwColor à partir de la définition de thème.  <br/> |
|«ShadowTransparency»  <br/> |Récupère la valeur de la cellule ShdwColorTrans à partir de la définition de thème.  <br/> |
|«ShadowMagnification»  <br/> |Récupère la valeur de la cellule ShapeShdwScaleFactor à partir de la définition de thème.  <br/> |
|«ShadowBlur»  <br/> |Récupère la valeur de la cellule ShapeShdwBlur à partir de la définition de thème.  <br/> |
|«ShadowXOffset»  <br/> |Récupère la valeur de cellule ShapeShdwOffsetX à partir de la définition de thème.  <br/> |
|«ShadowYOffset»  <br/> |Récupère la valeur de la cellule ShapeShdwOffsetY à partir de la définition de thème.  <br/> |
|«ShadowDirection»  <br/> |Récupère la valeur de la cellule ShapeShdwObliqueAngle à partir de la définition du thème.  <br/> |
|«ShadowPattern»  <br/> |Récupère la valeur de la cellule ShdwPattern dans la définition du thème.  <br/> |
|BevelTopType  <br/> |Récupère la valeur de la cellule BevelTopType à partir de la définition de thème.  <br/> |
|BevelTopWidth  <br/> |Récupère la valeur de la cellule BevelTopWidth à partir de la définition de thème.  <br/> |
|BevelTopHeight  <br/> |Récupère la valeur de la cellule BevelTopHeight à partir de la définition de thème.  <br/> |
|«BevelMaterial»  <br/> |Récupère la valeur de la cellule BevelMaterialType à partir de la définition de thème.  <br/> |
|«BevelLighting»  <br/> |Récupère la valeur de la cellule BevelLightingType à partir de la définition de thème.  <br/> |
|BevelLightingAngle  <br/> |Récupère la valeur de la cellule BevelLightingAngle à partir de la définition de thème.  <br/> |
|BevelContourColor  <br/> |Récupère la valeur de la cellule BevelContourColor à partir de la définition de thème.  <br/> |
|BevelContourSize  <br/> |Récupère la valeur de la cellule BevelContourSize à partir de la définition de thème.  <br/> |
|ReflectionBlur  <br/> |Récupère la valeur de la cellule ReflectionBlur à partir de la définition de thème.  <br/> |
|ReflectionDist  <br/> |Récupère la valeur de la cellule ReflectionDist à partir de la définition de thème.  <br/> |
|ReflectionSize  <br/> |Récupère la valeur de la cellule de réflexion à partir de la définition de thème.  <br/> |
|ReflectionTrans  <br/> |Récupère la valeur de la cellule ReflectionTrans à partir de la définition de thème.  <br/> |
|SoftEdgesSize  <br/> |Récupère la valeur de la cellule SoftEdgesSize à partir de la définition de thème.  <br/> |
|GlowSize  <br/> |Récupère la valeur de la cellule GlowSize à partir de la définition de thème.  <br/> |
|GlowColor  <br/> |Récupère la valeur de la cellule GlowColor à partir de la définition de thème.  <br/> |
|«GlowTransparency»  <br/> |Récupère la valeur de la cellule GlowColorTrans à partir de la définition de thème.  <br/> |
|SketchAmount  <br/> |Récupère la valeur de la cellule SketchAmount à partir de la définition de thème.  <br/> |
|SketchEnabled  <br/> |Récupère la valeur de la cellule SketchEnabled à partir de la définition de thème.  <br/> |
|SketchFillChange  <br/> |Récupère la valeur de la cellule SketchFillChange à partir de la définition de thème.  <br/> |
|SketchLineChange  <br/> |Récupère la valeur de la cellule SketchLineChange à partir de la définition de thème.  <br/> |
|SketchLineWeight  <br/> |Récupère la valeur de la cellule SketchLineWeight à partir de la définition de thème.  <br/> |
|«LatinFont»  <br/> |Récupère la valeur de la cellule de police à partir de la définition de thème.  <br/> |
|TextColor  <br/> |Récupère la valeur de la cellule de couleur à partir de la définition de thème.  <br/> |
|Attribuer  <br/> |Récupère la valeur de la cellule Character. style à partir de la définition de thème.  <br/> |
|«ComplexFont»  <br/> |Récupère la valeur de la cellule ComplexScriptFont à partir de la définition de thème.  <br/> |
|AsianFont  <br/> |Récupère la valeur de la cellule AsianFont à partir de la définition de thème.  <br/> |
|"FillStop [x] couleur"  <br/> |Récupère la valeur de la cellule de couleur dans la ligne *x* à partir de la définition de thème.  <br/> |
|"FillStop [x] transparence"  <br/> |Récupère la valeur de la cellule ColorTrans de la ligne *x* à partir de la définition de thème.  <br/> |
|«FillStop [x] position»  <br/> |Récupère la valeur de la cellule position de la ligne *x* à partir de la définition du thème.  <br/> |
|"LineStop [x] couleur"  <br/> |Récupère la valeur de la cellule de couleur dans la ligne *x* à partir de la définition de thème.  <br/> |
|"LineStop [x] transparence"  <br/> |Récupère la valeur de la cellule ColorTrans de la ligne *x* à partir de la définition de thème.  <br/> |
|«LineStop [x] position»  <br/> |Récupère la valeur de la cellule position de la ligne *x* à partir de la définition du thème.  <br/> |
   
## <a name="example"></a>Exemple

 `THEMEVAL("5")`
  
Renvoie la couleur accent 3 de la définition du thème.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Renvoie la valeur de la cellule «épaisseur» à partir de la définition de thème. Si aucun thème n'est appliqué à la forme contenant cette fonction, la fonction renvoie la valeur «0,7 PT».
  

