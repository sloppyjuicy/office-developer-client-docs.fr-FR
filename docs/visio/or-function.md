---
title: OR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Renvoie TRUE (1) si l’une des expressions logiques passées en tant que paramètres est TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433506"
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
  

