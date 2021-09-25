---
title: SUBSTITUTE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
ms.localizationpriority: medium
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Remplace une partie d’une chaîne de texte par une autre chaîne de texte.
ms.openlocfilehash: 88aeaff349e24d1b6a7e04470061e756acf6598e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559422"
---
# <a name="substitute-function"></a>Fonction SUBSTITUTE

Remplace une partie d’une chaîne de texte par une autre chaîne de texte. 
  
## <a name="syntax"></a>Syntaxe

 SUBSTITUTE (** *text* **, ** *old_text* **, ** *new_text* ** [, ** *start_num* ** ][, ** *ignore_case_opt* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte ou référence à une cellule contenant le texte dont vous souhaitez substituer des caractères.  <br/> |
| _old_text_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte à remplacer.  <br/> |
| _new_text_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte que vous souhaitez utiliser pour remplacer  _old_text_.  <br/> |
| _start_num_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Spécifie les occurrences des old_text à remplacer.  <br/> |
| _ignore_case_opt_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Valeur FALSE si la casse est respectée ; sinon, valeur TRUE. La valeur par défaut est FALSE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

 Si vous spécifiez  _start_num_opt_, seule cette occurrence de  _old_text_ est remplacée. Dans le cas contraire, chaque occurrence  _de old_text_  _dans_ le texte est modifiée en  _new_text._
  
Utilisez la fonction SUBSTITUTE lorsque vous souhaitez remplacer un texte spécifique dans une chaîne de texte. Si vous souhaitez remplacer le texte qui se trouve à un emplacement spécifique dans une chaîne de texte, utilisez la fonction REPLACE.
  
## <a name="example"></a>Exemple

SUBSTITUTE ("2 janvier 2003", "janvier", "JAN") 
  
Renvoie "2 JAN 2003". 
  
SUBSTITUTE ("2 janvier 2003","Janvier","JAN") 
  
Renvoie "2 janvier 2003". Aucune modification n’est apportée car la recherche respecte la casse. 
  

