---
title: Fonction THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs du document, où la couleur (numérique) transmise en tant qu'argument a été modifiée par la valeur de teinte ou d'ombrage stockée dans les paramètres de dégradé du thème actif.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332262"
---
# <a name="themecbv-function"></a>Fonction THEMECBV

Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs du document, où la couleur (numérique) transmise en tant qu'argument a été modifiée par la valeur de teinte ou d'ombrage stockée dans les paramètres de dégradé du thème actif. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **THEMECBV** ( _couleur_, _gradient_stop_number_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Number** <br/> |Un nombre représentant un index dans la palette de couleurs du document.  <br/> |
| _gradient_stop_number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Point de dégradé (teinte ou ombre) stocké dans les paramètres de dégradé du thème actif à appliquer à la couleur.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

 **Number**
  
## <a name="remarks"></a>Remarques

> [!NOTE]
> La fonction THEMECBV n'a aucun effet sur la couleur transmise en tant qu'argument si le QuickStyle affecté à la forme n'a pas de dégradé. 
  
Les paramètres de dégradé d'un thème sont une série de points de dégradé numérotés correspondant à une «éclaircie» (teinte) ou à un «assombrissement» (ombre). Ces nuances et teintes sont appliquées à une couleur de base pour créer un effet de couleur de dégradé.
  
La fonction **THEMECBV** prend une entrée de couleur et renvoie la couleur après qu'elle a été modifiée par la teinte ou l'ombrage du point de dégradé spécifié. Si le style rapide actif contient un remplissage en dégradé, les teintes et les ombres proviennent de la définition du thème. Si le style rapide actif ne spécifie pas de remplissage en dégradé ou si la forme n'est pas définie sur aucun thème, cette formule renvoie simplement la couleur qui a été transmise pour le premier argument. 
  
## <a name="example"></a>Exemple

 `THEMECBV(FillForegnd, 5)`
  
Renvoie la couleur créée en appliquant la teinte ou l'ombre du cinquième point de dégradé du dégradé à la couleur spécifiée dans la cellule **FillForegnd** . 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Renvoie une ombre ou teinte de rouge créée en appliquant le second point de dégradé à une couleur de base de rouge.
  

