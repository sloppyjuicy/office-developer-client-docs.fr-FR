---
title: SETATREFEXPR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
ms.localizationpriority: medium
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Stocke une valeur définie par le biais d’une action dans l’interface utilisateur (IU) ou Automation.
ms.openlocfilehash: 027a566db3c244118106422f3858312f9d703fe8
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405913"
---
# <a name="setatrefexpr-function"></a>Fonction SETATREFEXPR

Stocke une valeur définie par le biais d’une action dans l’interface utilisateur (IU) ou Automation.
  
## <a name="syntax"></a>Syntaxe

SETATREFEXPR ([ ***expr_opt* * ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expr_opt* <br/> |Facultatif  <br/> |**Varie** <br/> |Expression remplacée par la valeur ou l’expression affectée à la cellule référencée dans la fonction SETATREF. S’il n’est pas indiqué, sa valeur initiale est 0 (zéro). |

## <a name="remarks"></a>Remarques

La valeur d’une expression SETATREFEXPR peut également être définie à partir d’une fonction SETATREF dans une autre cellule référençant la cellule qui contient l’expression SETATREFEXPR.
  
Vous n’êtes pas limité à l’utilisation de la fonction SETATREFEXPR comme paramètre de la fonction SETATREF.
  
## <a name="example-1"></a>Exemple 1

L’exemple suivant utilise la fonction SETATREFEXPR pour garantir qu’une forme est aussi large que son texte.
  
Width =MAX(TEXTWIDTH(Texte),SETATREFEXPR())
  
## <a name="example-2"></a>Exemple 2

L’exemple suivant indique comment utiliser la fonction SETATREFEXPR pour que vos formes s’alignent sur une grille personnalisée. Les formules SETATREFEXPR sont placées dans les cellules PinX et PinY, entraînant l’alignement de l’axe de la forme sur la grille définie dans User.GridX et User.GridY.
  
User.GridX =2 mm
  
User.GridY =2 mm
  
PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX
  
PinY =INT(SETATREFEXPR()/User.Gridy + .5)\*User.Gridy
  
## <a name="example-3"></a>Exemple 3

Pour un exemple utilisant la fonction SETATREFEXPR avec la fonction SETATREF, reportez-vous à la fonction [SETATREF](setatref-function.md).
  