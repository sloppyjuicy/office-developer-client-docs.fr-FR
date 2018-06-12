---
title: TONE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifie la couleur en diminuant sa saturation de la quantité spécifiée dans le paramètre int.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789921"
---
# <a name="tone-function"></a>TONE, fonction

Modifie la couleur en diminuant sa saturation de la quantité spécifiée dans le paramètre _int_ . 
  
## <a name="syntax"></a>Syntaxe

TONE (** *couleur* **, ** *int* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Valeur de diminution de la saturation de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **RGB**
  
## <a name="remarks"></a>Note

Les limites supérieures et inférieures de saturation sont respectivement 0 et 240. Il n’existe aucune limite la taille de l’entier, que vous pouvez passer au paramètre _int_ , mais la saturation ne dépasse jamais ces limites. 
  

