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
description: Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte recherché par rapport à sa position dans la chaîne de texte qui le contient.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788659"
---
# <a name="find-function"></a>FIND, fonction

Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte recherché par rapport à sa position dans la chaîne de texte qui le contient.
  
## <a name="syntax"></a>Syntaxe

Rechercher (** *rechercher_texte* **, ** *within_text* **, [** *start_num* **], [** *ignorer_casse* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _rechercher_texte_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chaîne de texte à rechercher.  <br/> |
| _format_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chaîne de texte qui contient le texte à rechercher.  <br/> |
| _Start_num_ <br/> |Facultatif  <br/> |**Number** <br/> |Le caractère à partir duquel commencer la recherche. Le premier caractère de _dans_texte_ est 1. Si _start_num_ est manquant, il est supposé pour être 1.  <br/> |
| _ignorer_casse_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Par défaut, la fonction FIND respecte la casse. Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Remarques

Si plusieurs correspondances sont trouvées, la fonction FIND renvoie la position de départ de la première correspondance dans la chaîne. L’argument _rechercher_texte_ ne considère aucun caractère comme des caractères génériques. 
  
Si _find_text_:
  
-  Est vide (« »), FIND renvoie le premier caractère de la chaîne recherchée (c'est-à-dire, le caractère numéroté _num_départ_ ou 1). 
    
- N’apparaît pas dans _dans_texte_, FIND renvoie la #VALUE ! valeur d’erreur. 
    
Si _start_num_:
  
- n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR! ; 
    
- Est supérieur à la longueur de _dans_texte_, Find renvoie la #VALUE ! valeur d’erreur. 
    
## <a name="example"></a>Exemple

FIND ("2003";"20 janvier 2003") 
  
Renvoie 12. 
  

