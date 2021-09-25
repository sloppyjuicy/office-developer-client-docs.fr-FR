---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
ms.localizationpriority: medium
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Renvoie le ou les derniers caractères d’une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 4b4a2cb68f6e15989fade7088e887f852ac4eee8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573515"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Renvoie le ou les derniers caractères d’une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> | Chaîne de texte contenant les caractères à extraire.  <br/> |
| _num_chars_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Nombre de caractères à extraire. La valeur par défaut est 1.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de  _num_chars_opt_ doit être supérieure ou égale à zéro (0). 
  
Si  _num_chars_opt_ est supérieure à la longueur du texte, right renvoie tout le texte. Si  _num_chars_opt_ est omis, il est supposé être 1. 
  
## <a name="example"></a>Exemple

RIGHT ("Janvier 1; 2004"; 4) 
  
Renvoie la valeur 2004. 
  

