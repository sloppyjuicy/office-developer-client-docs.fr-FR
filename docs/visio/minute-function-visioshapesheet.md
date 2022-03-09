---
title: MINUTE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
ms.localizationpriority: medium
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Renvoie un nombre integer entre 0 et 59 qui représente le composant minutes de date/heure ou d’expression .
ms.openlocfilehash: e729616e8f5cda83f8efc11adc3fefb3ae80f137
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374032"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE Function (VisioShapeSheet)

Renvoie un nombre integer de 0 à 59 qui représente le composant minutes de *date/* heure ou d’expression.
  
## <a name="syntax"></a>Syntaxe

MINUTE( » *datetime*  « |  *expression*  [,  *lcid*  ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *datetime* <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| *expression* <br/> |Obligatoire  <br/> |**String** <br/> | Toute expression qui génère une date et une heure. |
| *lcid* <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |

### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant date dans *datetime* et *expression* n’est pas pris en compte.
  
Aucun arrondissement n’est effectué. Si l’argument *datetime* est introuvable ou ne peut pas être converti en un résultat valide, une erreur est renvoyée.
  
La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation.
  
La fonction MINUTE accepte également une valeur numérique simple pour *expression* où la partie décimale du résultat représente la fraction du jour depuis minuit.
  
## <a name="example-1"></a>Exemple 1

MINUTE(« 7/7/1999 13:45:24 »)
  
Renvoie 45.
  
## <a name="example-2"></a>Exemple 2

MINUTE(VALEURHEURE("25 janv. 1999 12:07:45") + 6 me.)
  
Renvoie 13.
  
## <a name="example-3"></a>Exemple 3

MINUTE(0,575)
  
Renvoie 48.
  