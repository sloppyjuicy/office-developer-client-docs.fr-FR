---
title: SAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
ms.localizationpriority: medium
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Renvoie la valeur du composant de saturation d’une couleur.
ms.openlocfilehash: 619a221e1b22442605364ee8cdf1b29f3fc002c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627547"
---
# <a name="sat-function"></a>Fonction SAT

Renvoie la valeur du composant de saturation d’une couleur. 
  
## <a name="syntax"></a>Syntaxe

SAT(** *expression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 240 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.
  
## <a name="example-1"></a>Exemple 1

SAT(Sheet.4! FillForegnd)
  
Renvoie la composante Saturation de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

SAT(8)
  
Renvoie 240 si le document utilise la palette de couleurs par défaut de Visio où rouge foncé est la couleur de l’index 8.
  
## <a name="example-3"></a>Exemple 3

SAT(HSL(10, 20, 30))
  
Renvoie 20.
  

