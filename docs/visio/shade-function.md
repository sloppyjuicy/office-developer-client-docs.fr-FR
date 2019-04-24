---
title: SHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifie la couleur en diminuant sa luminosité de la valeur (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326595"
---
# <a name="shade-function"></a>Fonction SHADE

Modifie la couleur en diminuant sa luminosité de la valeur (positive ou négative) spécifiée dans le paramètre _int_ . 
  
## <a name="syntax"></a>Syntaxe

OMBRE (* * *couleur* * *, * * *int* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur de diminution de la luminosité de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RVB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de luminosité sont respectivement 0 et 240. Il n'y a pas de limite quant à la taille de l'entier que vous pouvez transmettre pour le paramètre _int_ , mais la luminosité ne dépasse jamais ces limites. 
  
![Limites inférieures et supérieures de luminosité](media/image199_ZA10173627.gif)
  

