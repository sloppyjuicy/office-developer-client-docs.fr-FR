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
description: Utilisé dans le set_expression de la fonction SETATREF pour indiquer que les set_expression doivent être évaluées avant d’affecter au paramètre de référence dans SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432981"
---
# <a name="setatrefeval-function"></a>Fonction SETATREFEVAL

Utilisé dans _le set_expression_ de la fonction SETATREF  pour indiquer que les set_expression doivent  être évaluées avant d’affecter au paramètre de référence dans SETATREF. 
  
## <a name="syntax"></a>Syntaxe

SETATREFEVAL(** *expr* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Expression évaluée lorsque la fonction SETATREF redirige set_expression  _vers_ une autre cellule.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous affectez *le paramètre set_expression* de la fonction SETATREF à  une cellule référencée, Microsoft Visio écrit set_expression dans la cellule en tant qu’expression par défaut. Toutefois, si une partie du paramètre  *set_expression*  est enveloppée par la fonction SETATREFEVAL, Visio évalue l’expression et remplace la fonction SETATREFEVAL par son résultat avant de résoudre l’expression SETATREF. 
  
## <a name="example"></a>Exemple

Pour un exemple, reportez-vous à la fonction [SETATREF](setatref-function.md). 
  

