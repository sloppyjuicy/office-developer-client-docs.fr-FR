---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
ms.localizationpriority: medium
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 7813f123ccd349c3122aa02449f5ed5d9a7038a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623340"
---
# <a name="mid-function-visioshapesheet"></a>MID Function (VisioShapeSheet)

Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

MID (** *text* **, ** *start_num* **, ** *num_chars* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire.  <br/> |
| _start_num_ <br/> |Obligatoire  <br/> |**Number** <br/> |Position du premier caractère à extraire. Le premier caractère de la chaîne de texte est à la position 1.  <br/> |
| _num_chars_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de caractères à renvoyer.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si  *start_num*  est : 
  
- Supérieur à la longueur du  *texte*  , MID renvoie «  » (texte vide). 
    
- Inférieur à la longueur du  *texte,*  mais  *start_num*  plus  *num_chars*  dépasse la longueur du texte  *,*  MID renvoie les caractères jusqu’à la fin du  *texte*  . 
    
- inférieur à 1, MID renvoie la valeur d’erreur #VALEUR!. 
    
Si  *num_chars*  est négatif, MID renvoie la valeur #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
  
## <a name="example"></a>Exemple

MID ("SSN 999-99-9999";5;11) 
  
Renvoie 999-99-9999. 
  

