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
description: Renvoie le ou les caractères les plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: c2780fcaa6c60b8b801938bbd194796dd4f00c24
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783214"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Renvoie le ou les caractères les plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

LEFT(** *text* **, [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Requis  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire. |
| _num_chars_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Nombre de caractères à extraire. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de  _num_chars_opt_ doit être supérieure ou égale à zéro (0). 
  
Si  _num_chars_opt_ est supérieure à la longueur du texte, left renvoie tout le texte. Si  _num_chars_opt_ est omis, il est supposé être 1. 
  
## <a name="example"></a>Exemple

LEFT ("Janvier 1 2004", 3) 
  
Renvoie la valeur "Jan". 
  

