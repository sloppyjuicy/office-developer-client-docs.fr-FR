---
title: DAY Function (VisioShapeSheet)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
ms.localizationpriority: medium
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Renvoie un integer, de 1 à 31, qui représente le jour dans l’expression ou l’heure de date. La fonction DAY utilise le calendrier grégorien.
ms.openlocfilehash: 95b5ce70d05485822aee3683fba0293d559da6f5
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507104"
---
# <a name="day-function-visioshapesheet"></a>DAY Function (VisioShapeSheet)

Renvoie un integer, de 1 à 31, qui représente le jour dans _l’expression ou l’heure de date_. La fonction DAY utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DAY( » ***datetime** _ « | _*_expression_*_ [, _ *_lcid_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Requis  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Requis  <br/> |**String** <br/> |Toute expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |

### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Les composants d’heure figurant dans les paramètres _datetime_ ou _expression_ ne sont pas pris en compte.
  
Aucun arrondissement n’est effectué. Si l’argument _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, une erreur est renvoyée.
  
La fonction DAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.
  
## <a name="example-1"></a>Exemple 1

DAY("30 mai 1997 15:45:24")
  
Renvoie 30.
  
## <a name="example-2"></a>Exemple 2

DAY(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 6.
  
## <a name="example-3"></a>Exemple 3

DAY(35580.6337)
  
Renvoie 30.
  