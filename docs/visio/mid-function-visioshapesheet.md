---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Renvoie un nombre spécifique de caractères d'une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360661"
---
# <a name="mid-function-visioshapesheet"></a>MID Function (VisioShapeSheet)

Renvoie un nombre spécifique de caractères d'une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

MID (* * *texte* * *, * * *no_départ* * *, * * *no_car* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire.  <br/> |
| _no_départ_ <br/> |Obligatoire  <br/> |**Number** <br/> |Position du premier caractère à extraire. Le premier caractère de la chaîne de texte est à la position 1.  <br/> |
| _no_car_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de caractères à renvoyer.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si *no_départ* est: 
  
- Supérieur à la longueur de *Text* , MID renvoie "" (texte vide). 
    
- Inférieur à la longueur de *texte* , mais *no_départ* plus *no_car* dépasse la longueur de ** texte, MID renvoie les caractères jusqu'à la fin du *texte* . 
    
- Inférieur à 1, MID renvoie la #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
    
Si *no_car* est négatif, MID renvoie la #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
  
## <a name="example"></a>Exemple

MID ("SSN 999-99-9999";5;11) 
  
Renvoie 999-99-9999. 
  

