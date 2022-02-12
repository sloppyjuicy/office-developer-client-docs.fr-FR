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
ms.openlocfilehash: 9b112507db51bb84bd0aa005c47f9fbdc715f76b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775496"
---
# <a name="mid-function-visioshapesheet"></a>MID Function (VisioShapeSheet)

Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

MID (** *text* **, ** *start_num* **, ** *num_chars* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Requis  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire. |
| _start_num_ <br/> |Requis  <br/> |**Number** <br/> |Position du premier caractère à extraire. Le premier caractère de la chaîne de texte est à la position 1. |
| _num_chars_ <br/> |Requis  <br/> |**Number** <br/> |Nombre de caractères à renvoyer. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si  *start_num*  est : 
  
- Supérieur à la longueur du  *texte*  , MID renvoie «  » (texte vide). 
    
- Inférieur à la longueur du  *texte, mais*  *start_num*  plus  *num_chars*  dépasse la longueur du  *texte , MID*  renvoie les caractères jusqu’à la fin du  *texte*  . 
    
- inférieur à 1, MID renvoie la valeur d’erreur #VALEUR!. 
    
Si  *num_chars*  est négatif, MID renvoie la valeur #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
  
## <a name="example"></a>Exemple

MID ("SSN 999-99-9999";5;11) 
  
Renvoie 999-99-9999. 
  

