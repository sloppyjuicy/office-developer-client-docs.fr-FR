---
title: FIND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322497"
---
# <a name="find-function"></a>Fonction FIND

Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
  
## <a name="syntax"></a>Syntaxe

Find (* * *texte_cherché* * *, * * *dans_texte* * *, [* * *no_départ* * *], [* * *ignore_case* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _accepte_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte à rechercher.  <br/> |
| _format_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte qui contient le texte à rechercher.  <br/> |
| _no_départ_ <br/> |Facultatif  <br/> |**Number** <br/> |Caractère auquel débute la recherche. Le premier caractère dans _dans_texte_ est 1. Si _no_départ_ est manquant, il est supposé égal à 1.  <br/> |
| _ignore_case_ <br/> |Facultatif  <br/> |**Booléen** <br/> |Par défaut, la fonction FIND respecte la casse. Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si la fonction FIND détecte plusieurs correspondances, elle renvoie la position de début de la première chaîne. L'argument _texte_cherché_ ne tient pas compte des caractères génériques. 
  
Si _texte_cherché_:
  
-  Est vide (""), FIND correspond au premier caractère de la chaîne de recherche (c'est-à-dire, le caractère numéroté _no_départ_ ou 1). 
    
- N'apparaît pas dans _dans_texte_, Find renvoie la #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
    
Si _no_départ_:
  
- n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR! ; 
    
- Est supérieur à la longueur de _dans_texte_, FINDreturns le #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!. 
    
## <a name="example"></a>Exemple

FIND ("2003";"20 janvier 2003") 
  
Renvoie 12. 
  

