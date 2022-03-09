---
title: GUARD, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
ms.localizationpriority: medium
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protège l’expression contre la suppression et le changement par des actions effectuées dans la fenêtre de dessin, telles que le déplacement, le resserrage, le regroupement ou la suppression de formes.
ms.openlocfilehash: c0fa800c959853694cce8d77e2578ad1148aa105
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403436"
---
# <a name="guard-function"></a>Fonction GUARD

Protège  *l’expression*  contre la suppression et le changement par des actions effectuées dans la fenêtre de dessin, telles que le déplacement, le resserrage, le regroupement ou la suppression de formes.
  
## <a name="syntax"></a>Syntaxe

GUARD(***expression*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**String** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. |

## <a name="remarks"></a>Remarques

Les cellules les plus souvent concernées par la fonction GUARD sont les cellules Width, Height, PinX et PinY.
  
La protection d’une formule dans n’importe quelle cellule empêche que la valeur de cette dernière ne soit modifiée par des actions exécutées dans la fenêtre de dessin. Une même action peut toutefois avoir une incidence sur plusieurs cellules et chacune d’elles doit être protégée pour éviter des modifications inattendues de l’aspect des formes.
  
## <a name="example"></a>Exemple

GUARD(TEXTWIDTH(TheText) + 0,5 po)
  
Cette expression dans la cellule Largeur de la section Transformation de la forme évite que l’expression (TEXTWIDTH(TheText) + 0,5 po) ne soit remplacée par une autre valeur lorsque la largeur de la forme est modifiée dans la fenêtre de dessin. La cellule TheText est générée lorsque la composition du texte de la forme qui y est associée est modifiée.
  