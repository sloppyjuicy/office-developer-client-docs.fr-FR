---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
ms.localizationpriority: medium
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Renvoie le ou les caractères les plus à gauche d’une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 31b690c231f59bed53b8d04b0a4298621a718101
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554508"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Renvoie le ou les caractères les plus à gauche d’une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

LEFT(** *text* **, [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire.  <br/> |
| _num_chars_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Nombre de caractères à extraire.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de  _num_chars_opt_ doit être supérieure ou égale à zéro (0). 
  
Si  _num_chars_opt_ est supérieure à la longueur du texte, left renvoie tout le texte. Si  _num_chars_opt_ est omis, il est supposé être 1. 
  
## <a name="example"></a>Exemple

LEFT ("Janvier 1 2004", 3) 
  
Renvoie la valeur "Jan". 
  

