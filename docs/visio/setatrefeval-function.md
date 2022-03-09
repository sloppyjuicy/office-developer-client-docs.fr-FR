---
title: SETATREFEVAL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
ms.localizationpriority: medium
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Utilisé dans le set_expression de la fonction SETATREF pour indiquer que les set_expression doivent être évaluées avant d’affecter au paramètre de référence dans SETATREF.
ms.openlocfilehash: 8bd81cf653164d75e47eac63c439b70fa616e9b0
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379268"
---
# <a name="setatrefeval-function"></a>Fonction SETATREFEVAL

Utilisé dans _le set_expression_ de la fonction SETATREF pour indiquer que les set_expression doivent être  évaluées avant d’affecter au paramètre de référence dans SETATREF.
  
## <a name="syntax"></a>Syntaxe

SETATREFEVAL(***expr*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Expression évaluée lorsque la fonction SETATREF redirige  _set_expression vers une_ autre cellule. |

## <a name="remarks"></a>Remarques

En assignant le paramètre *set_expression* de la fonction SETATREF à une cellule référencée, Microsoft Visio écrit  *set_expression* dans la cellule comme une expression par défaut. Toutefois, si une partie du paramètre *set_expression* est enveloppée par la fonction SETATREFEVAL, Visio évalue l’expression et remplace la fonction SETATREFEVAL par son résultat avant de résoudre l’expression SETATREF.
  
## <a name="example"></a>Exemple

Pour un exemple, reportez-vous à la fonction [SETATREF](setatref-function.md).
