---
title: FORMATEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Renvoie le résultat d’expression calculé en unité srcUnit sous forme de chaîne mise en forme selon le format exprimé en dstUnit.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788692"
---
# <a name="formatex-function"></a>FORMATEX, fonction

Renvoie le résultat d’expression calculé en unité srcUnit sous forme de chaîne mise en forme selon le format exprimé en dstUnit.
  
## <a name="syntax"></a>Syntaxe

FORMATEX (** *expression* **, « ** *format* ** », [** *srcUnit* **], [** *dstUnit* **], [** *langID* **] [, ** *calID* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.  <br/> |
| _format_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Le format de l’image utilisée pour la chaîne de format. Pour plus d’informations sur les modèles de format, consultez la rubrique [Sur les modèles de Format](about-format-pictures.md).  <br/> |
| _srcUnit_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Unités utilisées pour calculer expression (po, cm, etc.).  <br/> |
| _dstUnit_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Unités à utiliser pour le résultat d’expression (po, cm, etc.).  <br/> |
| _ID de langue_ <br/> |Facultatif  <br/> |**Number** <br/> |Langue utilisée lors de la mise en forme des dates/heures de Microsoft Office System.  <br/> |
| _calID_ <br/> |Facultatif  <br/> |**Number** <br/> |Calendrier utilisé lors de la mise en forme des dates/heures de Microsoft Office System.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et le type spécifié dans le modèle de format régissent le comportement de la chaîne retournée. Le format doit être approprié pour le type d’expression.
  
L’argument srcUnit est utilisé à l’échelle des résultats d’expressions non typées, telles que 3 + 4. Si le résultat d’expression est un type explicite, tel que 3 ft + 8 ft, l’argument srcUnit est ignoré.
  
L’argument dstUnit est utilisé pour spécifier les unités utilisées pour le résultat de la mise en forme. Si dstUnit n’est pas spécifié, les unités pour le résultat de l’expression sont utilisées.
  
Renvoie une erreur si le résultat de l’expression et le type attendu dans format est de même nature, s’il existe des erreurs de syntaxe dans format, ou si elle ne reconnaît pas les unités transmise dans les arguments srcUnit ou dstUnit.
  
## <a name="example"></a>Exemple

FORMATEX(5,5, "0,00 u", "cm", "m") 
  
Renvoie 0,06 mètre. 
  

