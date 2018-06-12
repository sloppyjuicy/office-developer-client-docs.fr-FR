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
description: Renvoie la valeur du composant de luminosité d’une couleur.
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789056"
---
# <a name="lum-function"></a>LUM, fonction

Renvoie la valeur du composant de luminosité d’une couleur.
  
## <a name="syntax"></a>Syntaxe

LUM (** *expression* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index d’une couleur de la table des couleurs du document ou référence à une cellule qui contient un index de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

La valeur renvoyée est un nombre compris entre 0 et 240 inclus. La fonction renvoie 0 si l’entrée n’est pas valide. 
  
## <a name="example-1"></a>Exemple 1

LUM (feuille.4 ! FillForegnd)
  
Renvoie la composante luminosité de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

LUM(6)
  
Renvoie 120 si le document utilise la palette de couleurs par défaut de Visio où magenta est la couleur correspondant à l’index 6.
  
## <a name="example-3"></a>Exemple 3

LUM(HSL(10, 20, 30))
  
Renvoie 30.
  

