---
title: TONE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le paramètre int.
ms.openlocfilehash: 3bff72554a60706a1a8ceac9d60d914f5ec0791a
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404382"
---
# <a name="tone-function"></a>Fonction TONE

Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le _paramètre int_ .
  
## <a name="syntax"></a>Syntaxe

TONE(***color** _, _*_int_**)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur. |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur de diminution de la saturation de la couleur. Elle peut être positive ou négative. |

### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de saturation sont respectivement 0 et 240. Il n’existe pas de limite pour la taille de l’entier que vous pouvez envoyer au paramètre _int_, cependant la saturation ne dépasse jamais ces limites.
  