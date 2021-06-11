---
title: SUBSTITUTE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Remplace une partie d’une chaîne de texte par une autre chaîne de texte.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346822"
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
  

