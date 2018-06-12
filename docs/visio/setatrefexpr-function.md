---
title: SETATREFEXPR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Stocke une valeur qui est définie par une action dans l’interface utilisateur (IU) ou Automation.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789634"
---
# <a name="setatrefexpr-function"></a>SETATREFEXPR, fonction

Stocke une valeur qui est définie par une action dans l’interface utilisateur (IU) ou Automation.
  
## <a name="syntax"></a>Syntaxe

SETATREFEXPR ([** *expr_facult* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Facultatif  <br/> |**Varie** <br/> |Une expression est remplacée par la valeur ou l’expression affectée à la cellule référencée dans la fonction SETATREF. Si ne pas indiqué, sa valeur initiale est 0 (zéro).  <br/> |
   
## <a name="remarks"></a>Note

La valeur d’une expression SETATREFEXPR peut également être définie à partir d’une fonction SETATREF dans une autre cellule référençant la cellule qui contient l’expression SETATREFEXPR. 
  
Vous n’êtes pas limité à l’aide de la fonction SETATREFEXPR en tant que paramètre à la fonction SETATREF. 
  
## <a name="example-1"></a>Exemple 1

L’exemple suivant utilise la fonction SETATREFEXPR pour garantir qu’une forme est aussi large que son texte.
  
Width =MAX(TEXTWIDTH(Texte),SETATREFEXPR())
  
## <a name="example-2"></a>Exemple 2

L’exemple suivant indique comment utiliser la fonction SETATREFEXPR pour que vos formes s’alignent sur une grille personnalisée. Les formules SETATREFEXPR sont placées dans les cellules PinX et PinY, entraînant l’alignement de l’axe de la forme sur la grille définie dans User.GridX et User.GridY. 
  
User.GridX =2 mm
  
User.GridY =2 mm
  
PinX = INT (SETATREFEXPR () /User.GridX +.5)\*User.GridX
  
PinY = INT (SETATREFEXPR () /User.GridY +.5)\*User.GridY
  
## <a name="example-3"></a>Exemple 3

Pour obtenir un exemple utilisant la fonction SETATREFEXPR avec la fonction SETATREF, reportez-vous à la fonction [SETATREF](setatref-function.md) . 
  

