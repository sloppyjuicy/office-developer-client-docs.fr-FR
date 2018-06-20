---
title: SHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifie la couleur en diminuant sa luminosité d’une valeur (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789625"
---
# <a name="shade-function"></a>SHADE, fonction

Modifie la couleur en diminuant sa luminosité d’une valeur (positive ou négative) spécifiée dans le paramètre _int_ . 
  
## <a name="syntax"></a>Syntaxe

OMBRE (** *couleur* **, ** *int* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Valeur de diminution de la luminosité de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites supérieures et inférieures de luminosité sont respectivement 0 et 240. Il n’existe aucune limite la taille de l’entier, que vous pouvez passer au paramètre _int_ , mais la luminosité ne dépasse jamais ces limites. 
  
![](media/image199_ZA10173627.gif)
  

