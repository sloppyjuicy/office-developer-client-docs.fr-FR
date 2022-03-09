---
title: SHADE, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifie la couleur en réduisant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 9d19219b8f6744f5ceaab96d521ba9f7ff8d9dee
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405871"
---
# <a name="shade-function"></a>Fonction SHADE

Modifie la couleur en réduisant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int_ .
  
## <a name="syntax"></a>Syntaxe

SHADE(**_color_**, **_int_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur. |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur de diminution de la luminosité de la couleur. Elle peut être positive ou négative. |

### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de luminosité sont respectivement 0 et 240. Il n’existe pas de limite pour la taille de l’entier que vous pouvez envoyer au paramètre _int_, cependant la luminosité ne dépasse jamais ces limites.
  
![Limites supérieures et inférieures de luminosité](media/image199_ZA10173627.gif)
  