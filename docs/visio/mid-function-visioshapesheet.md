---
title: Fonction MID (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, selon le nombre de caractères que vous spécifiez.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789149"
---
# <a name="mid-function-visioshapesheet"></a>Fonction MID (VisioShapeSheet)

Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, selon le nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

MID (** *texte* **, ** *start_num* **, ** *nb_cars* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chaîne de texte qui contient les caractères à extraire.  <br/> |
| _Start_num_ <br/> |Obligatoire  <br/> |**Number** <br/> |Position du premier caractère à extraire. Le premier caractère de la chaîne de texte est à la position 1.  <br/> |
| _nb_cars_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de caractères à renvoyer.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Si *start_num* est : 
  
- Supérieur à la longueur de *texte* , MID renvoie « » (texte vide). 
    
- Inférieur à la longueur du *texte* , mais *start_num* plus *num_chars* dépasse la longueur du *texte* , MID renvoie les caractères jusqu'à la fin du *texte* . 
    
- inférieur à 1, MID renvoie la valeur d’erreur #VALEUR!. 
    
Si *nb_cars* est négatif, MID renvoie la #VALUE ! valeur d’erreur. 
  
## <a name="example"></a>Exemple

MID ("SSN 999-99-9999";5;11) 
  
Renvoie 999-99-9999. 
  

