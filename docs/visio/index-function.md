---
title: INDEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
ms.localizationpriority: medium
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Renvoie la sous-stration à l’index d’emplacement de base zéro dans la liste délimitée par le délimiteur. Ou, si l’index est en dehors de la plage, renvoie une chaîne vide ou le jeton facultatif fourni en tant qu’argument valeur d’erreur.
ms.openlocfilehash: 09559640a9d3b1d1da730a125024c9a8f4a11699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628135"
---
# <a name="index-function"></a>Fonction INDEX

Renvoie la sous-stration à  _l’index_ d’emplacement de base zéro dans la  _liste_ délimitée par  _le délimiteur_. Ou, si l’index est en dehors de la plage, renvoie une chaîne vide ou le jeton facultatif fourni en tant qu’argument *valeur d’erreur.* 
  
## <a name="syntax"></a>Syntaxe

INDEX(** *index* **, » ** *list* ** « [,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatoire  <br/> |**Number** <br/> |Emplacement à localiser.  <br/> |
| _list_ <br/> |Obligatoire  <br/> |**String** <br/> |Liste dans laquelle effectuer la recherche.  <br/> |
| _delimiter_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Chaîne à utiliser comme délimiteur dans la _liste._ Une  _chaîne de délimiteur_ peut comporter plusieurs caractères et inclure des caractères à plusieurs octets. La valeur par défaut est le point-virgule.  <br/> |
| _errorvalue_ <br/> |Facultatif  <br/> |**Number** <br/> | Valeur définie par l’utilisateur renvoyée si l’index est hors des limites admises. La valeur par défaut est une chaîne vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Si la liste commence ou se termine par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle. 
  
Si l’index est en dehors de la plage, Visio renvoie une chaîne vide ou le jeton facultatif fourni en tant qu’argument *valeur d’erreur.* 
  
## <a name="example-1"></a>Exemple 1

INDEX(3,"cat;rat;; ; ]
  
Renvoie « chèvre ».
  
## <a name="example-2"></a>Exemple 2

INDEX(54, »;1;2;3; »,,"ERROR »)
  
Renvoie « ERROR ».
  

