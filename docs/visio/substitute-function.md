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
description: Remplace une partie d’une chaîne de texte avec une autre chaîne de texte.
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789839"
---
# <a name="substitute-function"></a>SUBSTITUTE, fonction

Remplace une partie d’une chaîne de texte avec une autre chaîne de texte. 
  
## <a name="syntax"></a>Syntaxe

 SUBSTITUT (** *texte* **, ** *old_text* **, ** *new_text* ** [, ** *start_num* **] [, ** *ignorer_casse_opt* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Texte ou référence à une cellule contenant le texte dont vous souhaitez substituer des caractères.  <br/> |
| _old_text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Le texte que vous souhaitez remplacer.  <br/> |
| _new_text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Le texte que vous souhaitez utiliser pour remplacer _old_text_.  <br/> |
| _num_début_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Indique quelles occurrences de old_text remplacer.  <br/> |
| _ignorer_casse_opt_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Valeur FALSE si la casse est respectée ; sinon, valeur TRUE. La valeur par défaut est FALSE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

 Si vous spécifiez _num_début_opt_, seule cette occurrence _d’ancien_texte_ est remplacée. Dans le cas contraire, toutes les occurrences _old_text_ dans le _texte_ sont remplacé par _new_text._
  
Utilisez la fonction SUBSTITUTE lorsque vous souhaitez remplacer du texte spécifique dans une chaîne de texte. Si vous souhaitez remplacer du texte qui se produit dans un emplacement spécifique dans une chaîne de texte, utilisez la fonction REPLACE.
  
## <a name="example"></a>Exemple

SUBSTITUTE ("2 janvier 2003", "janvier", "JAN") 
  
Renvoie "2 JAN 2003". 
  
SUBSTITUTE ("2 janvier 2003","Janvier","JAN") 
  
Renvoie « 1 janvier 2003 ». Aucune modification n’est effectuée, car la recherche respecte la casse. 
  

