---
title: UPPER, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
ms.localizationpriority: medium
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: Renvoie une chaîne convertie en minuscules.
ms.openlocfilehash: e7f1ea62aa4311464561885214dd1cfe99a52aeb
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62769875"
---
# <a name="upper-function"></a>Fonction UPPER

Renvoie une chaîne convertie en minuscules.
  
## <a name="syntax"></a>Syntaxe

UPPER(** *expression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Requis  <br/> |**Varie** <br/> | Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en majuscules. |
   
## <a name="remarks"></a>Remarques

La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur. 
  
## <a name="example"></a>Exemple

UPPER("mAJ eT Min") 
  
Renvoie "MAJ ET MIN". 
  

