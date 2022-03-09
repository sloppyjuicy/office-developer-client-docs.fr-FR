---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
ms.localizationpriority: medium
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Renvoie un nombre integer, de 0 à 23, qui représente l’heure du jour du date/heure ou de l’expression.
ms.openlocfilehash: f5aa0e0eb66a102a64c093770434d3fc42a798a9
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404564"
---
# <a name="hour-function-visioshapesheet"></a>HOUR Function (VisioShapeSheet)

Renvoie un nombre integer, de 0 à 23, qui représente l’heure du jour du _date/_ heure ou de _l’expression_.
  
## <a name="syntax"></a>Syntaxe

HOUR( » **_datetime_** « | **_expression_** [, **_lcid_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Requis  <br/> |**String** <br/> | Chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Requis  <br/> |**Varie** <br/> |Expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> | Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |

## <a name="remarks"></a>Remarques

Le composant date dans _datetime_ et _expression_ n’est pas pris en compte.
  
Aucun arrondissement n’est effectué. Si l’argument _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, une erreur est renvoyée.
  
La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation.
  
La fonction HOUR accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit.
  
## <a name="example-1"></a>Exemple 1

HOUR(« 15:45 »)
  
Renvoie 15.
  
## <a name="example-2"></a>Exemple 2

HOUR("30 mai 1997 15:45:24")
  
Renvoie 15.
  
## <a name="example-3"></a>Exemple 3

HOUR(0,5)
  
Renvoie 12.
  
## <a name="example-4"></a>Exemple 4

HOUR(« 30/5/1997 »)
  
Renvoie 0.
  