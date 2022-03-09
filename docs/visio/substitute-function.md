---
title: SUBSTITUTE, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
ms.localizationpriority: medium
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Remplace une partie d’une chaîne de texte par une autre chaîne de texte.
ms.openlocfilehash: c39a1c86aae6fad2968d27aebb682df2bdc40e89
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404494"
---
# <a name="substitute-function"></a>Fonction SUBSTITUTE

Remplace une partie d’une chaîne de texte par une autre chaîne de texte.
  
## <a name="syntax"></a>Syntaxe

 SUBSTITUTE (***text** _, _*_old_text_*_, _*_new_text_*_ [, _*_start_num_*_ ][, _ *_ignore_case_opt_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *text* <br/> |Requis  <br/> |**String** <br/> | Texte ou référence à une cellule contenant le texte dont vous souhaitez substituer des caractères. |
| *old_text* <br/> |Requis  <br/> |**String** <br/> | Texte à remplacer. |
| *new_text* <br/> |Requis  <br/> |**String** <br/> | Texte par lequel remplacer *old_text*. |
| *start_num_opt* <br/> |Facultatif  <br/> |**Numérique** <br/> |Spécifie les occurrences des old_text à remplacer. |
| *ignore_case_opt* <br/> |Facultatif  <br/> |**Boolean** <br/> |Valeur FALSE si la casse est respectée ; sinon, valeur TRUE. La valeur par défaut est FALSE. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

 Si vous spécifiez *start_num_opt*, seule cette occurrence de *old_text* est remplacée. Sinon, chaque occurrence de *old_text* dans *text* est remplacée par *new_text*.
  
Utilisez la fonction SUBSTITUTE lorsque vous souhaitez remplacer un texte spécifique dans une chaîne de texte. Si vous souhaitez remplacer le texte qui se trouve à un emplacement spécifique dans une chaîne de texte, utilisez la fonction REPLACE.
  
## <a name="example"></a>Exemple

SUBSTITUTE ("2 janvier 2003", "janvier", "JAN")
  
Renvoie "2 JAN 2003".
  
SUBSTITUTE ("2 janvier 2003","Janvier","JAN")
  
Renvoie "2 janvier 2003". Aucune modification n’est apportée car la recherche respecte la casse.
  