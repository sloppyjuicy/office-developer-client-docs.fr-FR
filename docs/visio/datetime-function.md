---
title: DATETIME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
ms.localizationpriority: medium
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Renvoie la valeur de date et d’heure représentée par date/heure ou expression.
ms.openlocfilehash: 2d8d3bd17bf2c89b09b59a203bbe21a33bc6d8f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594635"
---
# <a name="datetime-function"></a>Fonction DATETIME

Renvoie la valeur de date et d’heure représentée par  _datetime_ ou  _expression_.
  
## <a name="syntax"></a>Syntaxe

DATETIME( » ** *datetime* ** « | ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Datetime
  
## <a name="remarks"></a>Remarques

Si  *datetime*  est manquante ou ne peut pas être interprétée comme une date ou une heure valide, DATETIME renvoie une #VALUE! erreur. 
  
La valeur renvoyée est formatée selon les formats d’heure et de date abrégés définis dans les paramètres régionaux actuels de votre système d’exploitation. 
  
La fonction DATETIME accepte également une valeur de nombre unique pour  *l’expression*  où la partie en nombres du résultat représente le nombre de jours depuis le 30 décembre 1899, et la partie décimale représente la fraction d’un jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

DATETIME("30 mai 1997") + 5 je.
  
Renvoie la valeur représentant le 04/06/97.
  
## <a name="example-2"></a>Exemple 2

FORMAT(DATETIME("20/05/1997 14:30:45"), "C")
  
Renvoie la chaîne « mardi 20 mai 1997 14:30:45 ».
  
## <a name="example-3"></a>Exemple 3

DATETIME("13:30 19 juillet")
  
Renvoie la valeur représentant 19/07/01 13:30 (en supposant que l’année actuelle soit 2001).
  
## <a name="example-4"></a>Exemple 4

DATETIME(35580.6337)
  
Renvoie la valeur représentant 30/05/97 15:12:32.
  

