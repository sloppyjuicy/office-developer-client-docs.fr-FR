---
title: HUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Renvoie la valeur du composant de teinte d’une couleur.
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788788"
---
# <a name="hue-function"></a>HUE, fonction

Renvoie la valeur du composant de teinte d’une couleur.
  
## <a name="syntax"></a>Syntaxe

TEINTE (** *expression* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Expression qui renvoie à une couleur.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

La valeur renvoyée est un nombre compris entre 0 et 239 inclus. L’entrée est l’index d’une couleur de la table du document, une expression qui produit une couleur personnalisée (telle que RVB ou TSL) ou une référence à une cellule contenant un index ou un résultat de couleurs. La fonction renvoie 0 si l’entrée n’est pas valide. 
  
## <a name="example-1"></a>Exemple 1

TEINTE (feuille.4 ! FillForegnd)
  
Renvoie la composante teinte de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

HUE(7)
  
Renvoie 120 si le document utilise la palette de couleurs par défaut de Microsoft Visio, où cyan est la couleur figurant à l’index 7.
  
## <a name="example-3"></a>Exemple 3

HUE(HSL(10, 20, 30) )
  
Renvoie 10.
  

