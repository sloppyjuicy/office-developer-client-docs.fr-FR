---
title: GREEN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Renvoie la composante verte d'une couleur.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438105"
---
# <a name="green-function"></a>Fonction GREEN

Renvoie la composante verte d'une couleur.
  
## <a name="syntax"></a>Syntaxe

VERT (* * *expression* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Réelle** <br/> |Un index d'une couleur dans la table des couleurs du document, une expression qui correspond à une couleur personnalisée (telle que RVB ou TSL) ou une référence à une cellule contenant un index ou un résultat de couleur.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index. Si *expression* n'est pas valide, elle renvoie 0 (noir). 
  
## <a name="example-1"></a>Exemple 1

VERT (feuille. 4! FillForegnd
  
Renvoie la composante verte de la couleur de remplissage de premier plan de feuille. couleur.
  
## <a name="example-2"></a>Exemple 2

VERT (11)
  
Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où jaune foncé est la couleur de l'index 11.
  
## <a name="example-3"></a>Exemple 3

VERT (RVB (10, 20, 30))
  
Renvoie 20.
  

