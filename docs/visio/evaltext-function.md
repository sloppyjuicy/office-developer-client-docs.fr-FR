---
title: EVALTEXT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
ms.localizationpriority: medium
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Évalue le texte dans le nom de la forme comme s’il s’agit d’une formule et renvoie le résultat.
ms.openlocfilehash: 3413adf189af1e623cd9911658cb38aa3d8d8070
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774318"
---
# <a name="evaltext-function"></a>Fonction EVALTEXT

Évalue le texte dans  _le nom de la forme_ comme s’il s’agit d’une formule et renvoie le résultat. 
  
## <a name="syntax"></a>Syntaxe

EVALTEXT(** *shapename!theText* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Requis  <br/> |**String** <br/> |Cellule générée lorsque la composition du texte de la forme associée est modifiée. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

 L’argument _shapename_ peut être utilisé pour faire référence au texte d’une forme autre que l’actuelle. 
  
En l’absence de texte, le résultat est zéro. Si le texte ne peut pas être calculé, la fonction renvoie une erreur.
  
## <a name="example"></a>Exemple

EVALTEXT(Line.2!theText) 
  
Évalue le texte contenu dans la forme Trait.2. Si, par exemple, Trait.2 contient « 121,92 cm + 15,24 cm », la valeur 137,16 cm est renvoyée. 
  

