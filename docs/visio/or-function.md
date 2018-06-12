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
description: Renvoie la valeur TRUE (1) si une des expressions logiques transmises en tant que paramètres est TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789194"
---
# <a name="or-function"></a>OR, fonction

Renvoie la valeur TRUE (1) si une des expressions logiques transmises en tant que paramètres est TRUE.
  
## <a name="syntax"></a>Syntaxe

OU (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Première expression dont vous souhaitez évaluer la véracité.  <br/> |
| _logicalexpression2_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Deuxième expression dont vous souhaitez évaluer la véracité.  <br/> |
| _logicalexpressionN_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Nième expression dont vous souhaitez évaluer la véracité.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Booléenne
  
## <a name="remarks"></a>Remarques

Une expression dont le calcul produit une valeur différente de zéro est considérée comme vraie (TRUE). Si toutes les expressions logiques sont fausses ou égales à 0, la fonction OR renvoie la valeur FALSE. 
  
## <a name="example"></a>Exemple

OU (hauteur \> 1, PinX \> 1) 
  
Renvoie TRUE (1) si l’une des expressions au moins a la valeur TRUE. Renvoie FALSE (0) seulement si les deux expressions sont fausses. 
  

