---
title: FORMAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
ms.localizationpriority: medium
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Renvoie le résultat de l’expression sous la forme d’une chaîne mise en forme en fonction de formatpicture.
ms.openlocfilehash: 142063e55be59b392eacbe168db3e3b9d780e5a6
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404805"
---
# <a name="format-function"></a>Fonction FORMAT

Renvoie le résultat de _l’expression_ sous la forme d’une chaîne mise en forme en fonction de _formatpicture_.
  
## <a name="syntax"></a>Syntaxe

FORMAT(***expression** _, » _ *_formatpicture_** « )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Requis  <br/> |**String** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. |
| _formatpicture_ <br/> |Requis  <br/> |**String** <br/> |Modèle de format utilisé pour la mise en forme de la chaîne. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée. L’argument _formatpicture_ doit convenir au type de l’expression. Pour plus d’informations sur la spécification d’images de format, voir [À propos des images de format](about-format-pictures.md).
  
Renvoie une erreur si le résultat de l’argument _expression_ et le type attendu dans l’argument _formatpicture_ ne sont pas de même nature ou si des erreurs de syntaxe se sont glissées dans _formatpicture_.
  
## <a name="example-1"></a>Exemple 1

FORMAT(1cm/4, "0,000 u")
  
Renvoie « 0,250 cm ».
  
## <a name="example-2"></a>Exemple 2

FORMAT(1cm/4, "0,00 U")
  
Renvoie « 0,25 CM ».
  
## <a name="example-3"></a>Exemple 3

FORMAT(1cm/4, "0,0 u")
  
Renvoie « 0,3 cm ».
  