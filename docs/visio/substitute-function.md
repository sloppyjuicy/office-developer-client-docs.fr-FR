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
description: Remplace une partie de chaîne de texte par une autre chaîne de texte.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346822"
---
# <a name="substitute-function"></a>Fonction SUBSTITUTE

Remplace une partie de chaîne de texte par une autre chaîne de texte. 
  
## <a name="syntax"></a>Syntaxe

 Substitut (* * *texte* * *, * * *ancien_texte* * *, * * *nouveau_texte* * * [, * * *no_départ* * *] [, * * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte ou référence à une cellule contenant le texte dont vous souhaitez substituer des caractères.  <br/> |
| _ancien_texte_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte à remplacer.  <br/> |
| _nouveau_texte_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte à utiliser pour remplacer _ancien_texte_.  <br/> |
| _start_num_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Indique les occurrences d'ancien_texte à remplacer.  <br/> |
| _ignore_case_opt_ <br/> |Facultatif  <br/> |**Booléen** <br/> |Valeur FALSE si la casse est respectée ; sinon, valeur TRUE. La valeur par défaut est FALSE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

 Si vous spécifiez _start_num_opt_, seule cette occurrence d' _ancien_texte_ est remplacée. Dans le cas contraire, toutes les occurrences d' _ancien_texte_ dans le _texte_ sont remplacées par _nouveau_texte._
  
Utilisez la fonction SUBSTITUTE lorsque vous souhaitez remplacer un texte spécifique dans une chaîne de texte. Si vous souhaitez remplacer le texte qui se trouve à un emplacement spécifique dans une chaîne de texte, utilisez la fonction rePLACE.
  
## <a name="example"></a>Exemple

SUBSTITUTE ("2 janvier 2003", "janvier", "JAN") 
  
Renvoie "2 JAN 2003". 
  
SUBSTITUTE ("2 janvier 2003","Janvier","JAN") 
  
Renvoie "2 janvier 2003". Aucune modification n’est apportée car la recherche respecte la casse. 
  

