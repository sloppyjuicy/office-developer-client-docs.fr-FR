---
title: TINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 212d7a8d3a09299bd3380d63e8b5039d9a0ff9c9
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463022"
---
# <a name="tint-function"></a>Fonction TINT

Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int_ . 
  
## <a name="syntax"></a>Syntaxe

TINT(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur d’augmentation de la luminosité de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de luminosité sont respectivement 0 et 240. Il n’y a aucune limite sur la taille de l’nombre  _integer_ que vous pouvez transmettre pour le paramètre int, mais la luminosité ne dépasse jamais ces limites. 
  

