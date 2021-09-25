---
title: FIND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
ms.localizationpriority: medium
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
ms.openlocfilehash: 313f6b97c5aacbb83e8aeedb91b69ce28cef465a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590197"
---
# <a name="find-function"></a>Fonction FIND

Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
  
## <a name="syntax"></a>Syntaxe

FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _find_text_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte à rechercher.  <br/> |
| _format_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte qui contient le texte à rechercher.  <br/> |
| _start_num_ <br/> |Facultatif  <br/> |**Number** <br/> |Caractère auquel débute la recherche. Le premier caractère de  _within_text_ est 1. Si  _start_num_ est manquant, il est supposé être 1.  <br/> |
| _ignore_case_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Par défaut, la fonction FIND respecte la casse. Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si la fonction FIND détecte plusieurs correspondances, elle renvoie la position de début de la première chaîne. _L find_text_ argument ne considère pas les caractères comme des caractères génériques. 
  
Si  _find_text_:
  
-  Est vide («  »), FIND correspond au premier caractère de la chaîne de recherche (autrement dit, le caractère numéro  _start_num_ ou 1). 
    
- N’apparaît pas  _dans within_text_, FIND renvoie la #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
    
Si  _start_num_:
  
- n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR! ; 
    
- Est supérieur à la longueur de  _within_text_, FINDreturns le #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
    
## <a name="example"></a>Exemple

FIND ("2003";"20 janvier 2003") 
  
Renvoie 12. 
  

