---
title: FORMATEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
ms.localizationpriority: medium
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Renvoie le résultat de l’expression évaluée dans srcUnit sous la forme d’une chaîne mise en forme selon le format exprimé dans dstUnit.
ms.openlocfilehash: 1e4aa50dcc9d3506fc4951455cbf92045033c5db
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405106"
---
# <a name="formatex-function"></a>Fonction FORMATEX

Renvoie le résultat de l’expression évaluée dans srcUnit sous la forme d’une chaîne mise en forme selon le format exprimé dans dstUnit.
  
## <a name="syntax"></a>Syntaxe

FORMATEX(***expression** _, » _*_format_*_ « ,[ _*_srcUnit_*_ ],[ _*_dstUnit_*_ ],[ _*_langID_*_ ][, _ *_calID_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**String** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. |
| *format* <br/> |Requis  <br/> |**String** <br/> |Image de format utilisée pour mettre en forme la chaîne. Pour plus d’informations sur les images de format, voir [À propos des images de format](about-format-pictures.md). |
| *srcUnit* <br/> |Facultatif  <br/> |**Chaîne** <br/> | Unités utilisées pour calculer expression (po, cm, etc.). |
| *dstUnit* <br/> |Facultatif  <br/> |**Chaîne** <br/> |Unités à utiliser pour le résultat d’expression (po, cm, etc.). |
| *langID* <br/> |Facultatif  <br/> |**Number** <br/> |Langue utilisée lors de la mise en forme des dates/heures de Microsoft Office System. |
| *calID* <br/> |Facultatif  <br/> |**Number** <br/> |Calendrier utilisé lors de la mise en forme des dates/heures de Microsoft Office System. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée. L’argument format doit convenir au type de l’expression.
  
L’argument srcUnit est utilisé pour mettre à l’échelle des résultats d’expressions non typées, telles que 3 + 4. Si le résultat d’expression est associé à un type précis, comme 3 m + 8 m, l’argument srcUnit est ignoré.
  
L’argument dstUnit est utilisé pour définir les unités employées dans le résultat mis en forme. Si dstUnit n’est pas précisé, les unités du résultat de l’expression sont utilisées.
  
Renvoie une erreur si le résultat d’expression et le type attendu dans format ne sont pas de même nature, si des erreurs de syntaxe se sont glissées dans format ou si les unités transmises dans les arguments srcUnit ou dstUnit ne sont pas reconnues.
  
## <a name="example"></a>Exemple

FORMATEX(5,5, "0,00 u", "cm", "m")
  
Renvoie 0,06 mètre.
  