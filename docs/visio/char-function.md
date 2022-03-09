---
title: CHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
ms.localizationpriority: medium
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Renvoie le caractère ANSI d’un nombre.
ms.openlocfilehash: adbc775ec310b41ddb5198e7709d0ec07269b605
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406245"
---
# <a name="char-function"></a>Fonction CHAR

Renvoie le caractère ANSI d’un nombre.
  
## <a name="syntax"></a>Syntaxe

CHAR(***number*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *number* <br/> |Requis  <br/> |**Number** <br/> |Nombre dont vous souhaitez obtenir le caractère ANSI. |

## <a name="remarks"></a>Remarques

La chaîne renvoyée comporte un seul caractère. Le paramètre *number* doit être un entier compris entre 1 et 255 (inclus), sinon la fonction renvoie une erreur.
  
## <a name="example"></a>Exemple

CHAR(9)
  
Renvoie le caractère de tabulation.
  