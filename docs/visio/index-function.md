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
description: Renvoie la sous-chaîne à l'index d'emplacement de base zéro dans la liste délimité par délimiteur. Ou, si l'index est en dehors de la plage, renvoie une chaîne vide ou le jeton facultatif fourni en tant qu'argument ERRORVALUE.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431574"
---
# <a name="index-function"></a>Fonction INDEX

Renvoie la sous-chaîne à l' _index_ d'emplacement de base zéro dans la _liste_ délimité __ par délimiteur. Ou, si l'index est en dehors de la plage, renvoie une chaîne vide ou le jeton facultatif fourni en tant qu'argument *ERRORVALUE* . 
  
## <a name="syntax"></a>Syntaxe

Index (* * *index* * *, "* * *List* * *" [, [* * ** Delimiter * *] [, [* * *ERRORVALUE* * *]]]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatoire  <br/> |**Number** <br/> |Emplacement à localiser.  <br/> |
| _liste_ <br/> |Obligatoire  <br/> |**String** <br/> |Liste dans laquelle effectuer la recherche.  <br/> |
| _delimiter_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Chaîne à utiliser en tant que délimiteur dans la _liste_. Une __ chaîne de délimiteur peut contenir plusieurs caractères et inclure des caractères multioctets. La valeur par défaut est le point-virgule.  <br/> |
| _ERRORVALUE_ <br/> |Facultatif  <br/> |**Number** <br/> | Valeur définie par l’utilisateur renvoyée si l’index est hors des limites admises. La valeur par défaut est une chaîne vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Si la liste commence ou se termine par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle. 
  
Si l'index est en dehors de la plage, Visio renvoie une chaîne vide ou le jeton facultatif fourni en tant qu'argument *ERRORVALUE* . 
  
## <a name="example-1"></a>Exemple 1

INDEX (3, "cat; rat;; chèvre ")
  
Renvoie « chèvre ».
  
## <a name="example-2"></a>Exemple 2

INDEX (54, "; 1; 2; 3;",, "ERREUR")
  
Renvoie «erreur».
  

