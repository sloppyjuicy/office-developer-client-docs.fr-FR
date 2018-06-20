---
title: SETATREFEVAL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Utilisé dans le paramètre set_expression de la fonction SETATREF pour indiquer que set_expression devrait être évalué avant d’affecter au paramètre reference dans SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789612"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL, fonction

Utilisé dans le paramètre _set_expression_ de la fonction SETATREF pour indiquer que _set_expression_ devrait être évalué avant d’affecter au paramètre _reference_ dans SETATREF. 
  
## <a name="syntax"></a>Syntaxe

SETATREFEVAL (** *expr* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Une expression qui est évaluée lorsque la fonction SETATREF redirige _set_expression_ vers une autre cellule.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous affectez le paramètre *set_expression* de la fonction SETATREF à une cellule référencée, Microsoft Visio écrit *set_expression* à la cellule comme une expression par défaut. Toutefois, si n’importe quelle partie du paramètre *set_expression* est encapsulée par la fonction SETATREFEVAL, Visio évalue l’expression et remplace la fonction SETATREFEVAL par son résultat avant de résoudre l’expression SETATREF. 
  
## <a name="example"></a>Exemple

Pour obtenir un exemple, reportez-vous à la fonction [SETATREF](setatref-function.md) . 
  

