---
title: BLEND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mélange deux couleurs dans les proportions spécifiées par le paramètre float.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788145"
---
# <a name="blend-function"></a>BLEND, fonction

Mélange deux couleurs dans les proportions spécifiées par le paramètre _float_ . 
  
## <a name="syntax"></a>Syntaxe

BLEND (** *color1* **, ** *color2* **, ** *float [0,1]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la première couleur.  <br/> |
| _color2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la deuxième couleur.  <br/> |
| _float [0,1]_ <br/> |Obligatoire  <br/> |**Float** <br/> |La proportion de fusion _color2_ et _color1_, respectivement. Nombre réel entre 0 et 1 (inclus).  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **RGB**
  
## <a name="remarks"></a>Remarques

La couleur renvoyée est déterminée par les proportions mélange _color2_ et _color1_, respectivement, comme spécifié par le paramètre _float_ . Par exemple, si _float_ est 0.25, la couleur renvoyée est composée de 75 % des _color1_ et de 25 % de _color2_. 
  
Une autre manière de penser est que la valeur de _type float_ correspondant au point le long du spectre de _color1_ à _color2_. Par conséquent, plus petits numéros (de la plus proche de zéro) pour _float_ produit fusion rapprocher à _color1_, tandis que les numéros plus grande (plus proche de 1) produire dégradés rapprocher en _color2_.
  

