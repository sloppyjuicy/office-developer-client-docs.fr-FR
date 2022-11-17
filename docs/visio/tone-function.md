---
title: TONE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le paramètre int.
ms.openlocfilehash: 46757d425e60af86f12ce543ee1c99509a4b3865
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465583"
---
# <a name="tone-function"></a>Fonction TONE

Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le _paramètre int_ . 
  
## <a name="syntax"></a>Syntaxe

TONE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur de diminution de la saturation de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de saturation sont respectivement 0 et 240. Il n’y a aucune limite sur la taille de l’nombre  _integer_ que vous pouvez transmettre pour le paramètre int, mais la saturation ne dépasse jamais ces limites. 
  

