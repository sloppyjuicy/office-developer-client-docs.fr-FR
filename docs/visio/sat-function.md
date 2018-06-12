---
title: SAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Renvoie la valeur du composant de saturation d’une couleur.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789591"
---
# <a name="sat-function"></a>SAT, fonction

Renvoie la valeur du composant de saturation d’une couleur. 
  
## <a name="syntax"></a>Syntaxe

SAM (** *expression* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Numérique
  
## <a name="remarks"></a>Note

La valeur renvoyée est un nombre compris entre 0 et 240 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.
  
## <a name="example-1"></a>Exemple 1

SAT (feuille.4 ! FillForegnd)
  
Renvoie la composante Saturation de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

SAT(8)
  
Renvoie 240 si le document utilise la palette de couleurs par défaut de Visio où rouge foncé est la couleur de l’index 8.
  
## <a name="example-3"></a>Exemple 3

SAT(HSL(10, 20, 30))
  
Renvoie 20.
  

