---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Renvoie le ou les derniers caractères d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326725"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Renvoie le ou les derniers caractères d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

Right (* * *texte* * * [, * * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> | Chaîne de texte contenant les caractères à extraire.  <br/> |
| _num_chars_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Nombre de caractères à extraire. La valeur par défaut est 1.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de _num_chars_opt_ doit être supérieure ou égale à zéro (0). 
  
Si _num_chars_opt_ est supérieur à la longueur du texte, Right renvoie tout le texte. Si _num_chars_opt_ est omis, il est considéré comme étant égal à 1. 
  
## <a name="example"></a>Exemple

RIGHT ("Janvier 1; 2004"; 4) 
  
Renvoie la valeur 2004. 
  

