---
title: BLEND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Fusionne deux couleurs dans la proportion spécifiée par le paramètre float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303296"
---
# <a name="blend-function"></a>Fonction BLEND

Fusionne deux couleurs dans la proportion spécifiée par le paramètre _float_ . 
  
## <a name="syntax"></a>Syntaxe

BLEND (* * *color1* * *, * * *color2* * *, * * *float [0, 1]* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la première couleur.  <br/> |
| _color2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la deuxième couleur.  <br/> |
| _flotteur [0, 1]_ <br/> |Obligatoire  <br/> |**Float** <br/> |Proportion de mélange de _color2_ et de _color1_, respectivement. Nombre réel entre 0 et 1 inclus.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RVB**
  
## <a name="remarks"></a>Remarques

La couleur renvoyée est déterminée par les proportions relatives dans lesquelles fusionner _color2_ et _color1_, respectivement, comme spécifié par le paramètre _float_ . Par exemple, si _float_ est 0,25, la couleur renvoyée est composée de 75% de _color1_ et de 25% de _color2_. 
  
Une autre façon de penser est que la valeur en _virgule flottante_ correspond au point le long du spectre de couleurs de _color1_ à _color2_. Par conséquent, des nombres plus petits (plus proches __ de zéro) pour les produits flottants produisent des fusions plus proches de la taille de _color1_, tandis que les grands nombres (plus de 1) produisent des fusions plus près de _color2_.
  

