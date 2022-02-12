---
title: SHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifie la couleur en réduisant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: a1e01807f9a12471a259efa7a12457a2e1f3d6c2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777011"
---
# <a name="shade-function"></a>Fonction SHADE

Modifie la couleur en réduisant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int_ . 
  
## <a name="syntax"></a>Syntaxe

SHADE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur. |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur de diminution de la luminosité de la couleur. Elle peut être positive ou négative. |
   
### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de luminosité sont respectivement 0 et 240. Il n’y a aucune limite sur la taille de l’nombre  _integer_ que vous pouvez transmettre pour le paramètre int, mais la luminosité ne dépasse jamais ces limites. 
  
![Limites supérieures et inférieures de luminosité](media/image199_ZA10173627.gif)
  

