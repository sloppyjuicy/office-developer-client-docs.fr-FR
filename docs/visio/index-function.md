---
title: INDEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Retourne la sous-chaîne dans l’index de l’emplacement de base zéro dans la liste délimitée par délimiteur. Ou, si l’index est hors plage, cette propriété renvoie une chaîne vide ou la valeur facultative fournie comme argument errorvalue.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788821"
---
# <a name="index-function"></a>INDEX, fonction

Retourne la sous-chaîne à l' emplacement de base zéro _index_ dans la _liste_ délimitée par _délimiteur_. Ou, si l’index est hors plage, cette propriété renvoie une chaîne vide ou la valeur facultative fournie comme argument *errorvalue* . 
  
## <a name="syntax"></a>Syntaxe

INDEX (** *index* **, « ** *liste* ** » [, [** *délimiteur* **] [, [** *errorvalue* **]]]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatoire  <br/> |**Number** <br/> |Emplacement à localiser.  <br/> |
| _liste_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Liste dans laquelle effectuer la recherche.  <br/> |
| _delimiter_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | La chaîne à utiliser comme délimiteur dans la _liste_. Une chaîne de _délimiteur_ peut comporter plusieurs caractères et inclure des caractères codés. La valeur par défaut est un point-virgule.  <br/> |
| _ERRORVALUE_ <br/> |Facultatif  <br/> |**Number** <br/> | Valeur définie par l’utilisateur renvoyée si l’index est hors des limites admises. La valeur par défaut est une chaîne vide.  <br/> |
   
## <a name="remarks"></a>Note

Si la liste commence ou se termine par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle. 
  
Si l’index est hors limites, Visio renvoie une chaîne vide ou la valeur facultative fournie comme argument *errorvalue* . 
  
## <a name="example-1"></a>Exemple 1

INDEX(3,"chat;rat;;chèvre")
  
Renvoie « chèvre ».
  
## <a name="example-2"></a>Exemple 2

INDEX(54,";1;2;3;",,"ERREUR")
  
Renvoie « Erreur ».
  

