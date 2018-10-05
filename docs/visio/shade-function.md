---
title: SHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifie la couleur en diminuant sa luminosité d’une valeur (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382980"
---
# <a name="shade-function"></a>Fonction SHADE

Modifie la couleur en diminuant sa luminosité d’une valeur (positive ou négative) spécifiée dans le paramètre _int_ . 
  
## <a name="syntax"></a>Syntaxe

OMBRE (** *couleur* **, ** *int* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numeric** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Valeur de diminution de la luminosité de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites supérieures et inférieures de luminosité sont respectivement 0 et 240. Il n’existe aucune limite la taille de l’entier, que vous pouvez passer au paramètre _int_ , mais la luminosité ne dépasse jamais ces limites. 
  
![Limites supérieure et inférieure de la luminosité](media/image199_ZA10173627.gif)
  

