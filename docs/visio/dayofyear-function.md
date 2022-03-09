---
title: DAYOFYEAR, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
ms.localizationpriority: medium
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Renvoie un nombre integer, de 1 à 366, qui représente le jour séquentiel de l’année dans l’expression ou le datetime. La fonction DAYOFYEAR utilise le calendrier grégorien.
ms.openlocfilehash: eb4f7dca59879d0970faeefe914926deff83bf94
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403899"
---
# <a name="dayofyear-function"></a>Fonction DAYOFYEAR

Renvoie un nombre integer, de 1 à 366, qui représente le jour séquentiel de l’année dans _l’expression_ ou le _datetime_. La fonction DAYOFYEAR utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DAYOFYEAR( » ***datetime** _ « | _*_expression_*_ [, _ *_lcid_** ])
  
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
  
Le résultat est compris entre le 1er janvier et le 31 décembre. Aucun arrondissement n’est effectué. Si l’argument _datetime_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, une erreur est renvoyée.
  
La fonction DAYOFYEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 31 décembre 1899.
  
## <a name="example-1"></a>Exemple 1

DAYOFYEAR("30 mai 1997 13:45:24")
  
Renvoie 150.
  
## <a name="example-2"></a>Exemple 2

DAYOFYEAR(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 157.
  
## <a name="example-3"></a>Exemple 3

DAYOFYEAR(35580.6337)
  
Renvoie 150.
  