---
title: TONE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le paramètre int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434374"
---
# <a name="tone-function"></a>Fonction TONE

Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le _paramètre int._ 
  
## <a name="syntax"></a>Syntaxe

TONE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur de diminution de la saturation de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RVB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de saturation sont respectivement 0 et 240. Il n’y a aucune limite sur la taille de l’nombre integer que vous pouvez transmettre pour le paramètre  _int,_ mais la saturation ne dépasse jamais ces limites. 
  

