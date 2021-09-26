---
title: OR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
ms.localizationpriority: medium
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Renvoie TRUE (1) si l’une des expressions logiques passées en tant que paramètres est TRUE.
ms.openlocfilehash: 3d625417b52f970cb529b300e8506835ba1b8990
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627806"
---
# <a name="or-function"></a>Fonction OR

Renvoie TRUE (1) si l’une des expressions logiques passées en tant que paramètres est TRUE.
  
## <a name="syntax"></a>Syntaxe

OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Obligatoire  <br/> |**String** <br/> |Première expression dont vous souhaitez évaluer la véracité.  <br/> |
| _logicalexpression2_ <br/> |Obligatoire  <br/> |**String** <br/> |Deuxième expression dont vous souhaitez évaluer la véracité.  <br/> |
| _logicalexpressionN_ <br/> |Obligatoire  <br/> |**String** <br/> |Nième expression dont vous souhaitez évaluer la véracité.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

Une expression dont le calcul produit une valeur différente de zéro est considérée comme vraie (TRUE). Si toutes les expressions logiques sont fausses ou égales à 0, la fonction OR renvoie la valeur FALSE. 
  
## <a name="example"></a>Exemple

OR(Height \> 1,PinX \> 1) 
  
Renvoie TRUE (1) si l’une des expressions au moins a la valeur TRUE. Renvoie FALSE (0) seulement si les deux expressions sont fausses. 
  

