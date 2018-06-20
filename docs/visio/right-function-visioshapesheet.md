---
title: Fonction RIGHT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Renvoie l’ou les derniers caractères dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789478"
---
# <a name="right-function-visioshapesheet"></a>Fonction RIGHT (VisioShapeSheet)

Renvoie l’ou les derniers caractères dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

DROITE (** *texte* ** [, ** *nb_cars_opt* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Chaîne de texte contenant les caractères à extraire.  <br/> |
| _nb_cars_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Nombre de caractères à extraire. La valeur par défaut est 1.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de _nb_cars_opt_ doit être supérieure ou égale à zéro (0). 
  
Si _nb_cars_opt_ est supérieur à la longueur du texte, RIGHT renvoie tout le texte. Si _nb_cars_opt_ est omis, il est supposé pour être 1. 
  
## <a name="example"></a>Exemple

RIGHT ("Janvier 1; 2004"; 4) 
  
Renvoie la valeur 2004. 
  

