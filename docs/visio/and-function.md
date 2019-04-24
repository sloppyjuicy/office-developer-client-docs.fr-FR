---
title: AND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies. Si l'une des expressions logiques est FALSe ou 0, la fonction et renvoie la valeur FALSe (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341558"
---
# <a name="and-function"></a>Fonction AND

Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies. Si l'une des expressions logiques est FALSe ou 0, la fonction et renvoie la valeur FALSe (0).
  
## <a name="syntax"></a>Syntaxe

et (* * *opérateur logique expression1* * *, * * caractères *logiques expression2* * *,..., * * *logical expression* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression logique_ <br/> |Obligatoire  <br/> |**String** <br/> | Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. Toute expression donnant une valeur différente de zéro est considérée comme vraie (valeur TRUE).  <br/> |
   
## <a name="example"></a>Exemple

ET (hauteur \> 1, PinX \> 1)
  
Renvoie TRUE si les deux expressions sont vraies. Renvoie FALSE si l’une des expressions est fausse.
  

