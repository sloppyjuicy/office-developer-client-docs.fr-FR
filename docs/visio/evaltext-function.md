---
title: EVALTEXT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Évalue le texte dans le nom de la forme comme s’il s’agit d’une formule et renvoie le résultat.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438357"
---
# <a name="evaltext-function"></a>Fonction EVALTEXT

Évalue le texte dans  _le nom de la forme_ comme s’il s’agit d’une formule et renvoie le résultat. 
  
## <a name="syntax"></a>Syntaxe

EVALTEXT(** *shapename!theText* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Obligatoire  <br/> |**String** <br/> |Cellule générée lorsque la composition du texte de la forme associée est modifiée.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

 L’argument _shapename_ peut être utilisé pour faire référence au texte d’une forme autre que l’actuelle. 
  
En l’absence de texte, le résultat est zéro. Si le texte ne peut pas être calculé, la fonction renvoie une erreur.
  
## <a name="example"></a>Exemple

EVALTEXT(Line.2!theText) 
  
Évalue le texte contenu dans la forme Trait.2. Si, par exemple, Trait.2 contient « 121,92 cm + 15,24 cm », la valeur 137,16 cm est renvoyée. 
  

