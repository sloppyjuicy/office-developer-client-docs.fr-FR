---
title: TINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406576"
---
# <a name="tint-function"></a>Fonction TINT

Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int._ 
  
## <a name="syntax"></a>Syntaxe

TINT(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur.  <br/> |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur d’augmentation de la luminosité de la couleur. Elle peut être positive ou négative.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RVB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de luminosité sont respectivement 0 et 240. Il n’y a aucune limite sur la taille de l’nombre integer que vous pouvez transmettre pour le paramètre  _int,_ mais la luminosité ne dépasse jamais ces limites. 
  

