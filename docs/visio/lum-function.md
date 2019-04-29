---
title: LUM, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Renvoie la valeur du composant de luminosité d'une couleur.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419337"
---
# <a name="lum-function"></a>Fonction LUM

Renvoie la valeur du composant de luminosité d'une couleur.
  
## <a name="syntax"></a>Syntaxe

LUM (* * *expression* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index d’une couleur de la table des couleurs du document ou référence à une cellule qui contient un index de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 240 inclus. La fonction renvoie 0 si l’entrée n’est pas valide. 
  
## <a name="example-1"></a>Exemple 1

LUM (feuille. 4! FillForegnd
  
Renvoie la composante luminosité de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

LUM (6)
  
Renvoie 120 si le document utilise la palette de couleurs par défaut de Visio où magenta est la couleur correspondant à l’index 6.
  
## <a name="example-3"></a>Exemple 3

LUM(HSL(10, 20, 30))
  
Renvoie 30.
  

