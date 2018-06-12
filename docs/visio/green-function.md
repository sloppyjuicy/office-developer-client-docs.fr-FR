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
description: Renvoie la composante verte d’une couleur.
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788764"
---
# <a name="green-function"></a>GREEN, fonction

Renvoie la composante verte d’une couleur.
  
## <a name="syntax"></a>Syntaxe

VERT (** *expression* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |L’index d’une couleur dans la table des couleurs du document, une expression qui correspond à une couleur personnalisée (comme RVB ou TSL) ou une référence à une cellule contenant un résultat de couleur index ou la couleur.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

La valeur de retour est un nombre compris entre 0 et 255, inclus, ou une référence de cellule qui correspond à un index. Si *l’expression* n’est pas valide, elle renvoie 0 (noir). 
  
## <a name="example-1"></a>Exemple 1

VERT (feuille.4 ! FillForegnd)
  
Renvoie la composante verte de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

GREEN(11)
  
Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio dans laquelle le jaune foncé est la couleur de l’index 11.
  
## <a name="example-3"></a>Exemple 3

GREEN(RVB(10, 20, 30))
  
Renvoie 20.
  

