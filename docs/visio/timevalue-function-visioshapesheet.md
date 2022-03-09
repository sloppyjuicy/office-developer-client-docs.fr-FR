---
title: TIMEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
ms.localizationpriority: medium
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Renvoie la valeur d’heure représentée par date/heure ou expression, en fonction des paramètres de région et de langue du système.
ms.openlocfilehash: d4b87697ce85626aa447df11f71d350735b949d3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380367"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE Function (VisioShapeSheet)

Renvoie la valeur d’heure représentée par _date/__heure ou expression_, en fonction des paramètres de région et de langue du système.
  
## <a name="syntax"></a>Syntaxe

TIMEVALUE( » ***datetime** _ « | _*_expression_*_ [, _ *_lcid_** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatoire  <br/> |**String** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Toute expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |
   
## <a name="remarks"></a>Remarques

Tout composant de date dans  _l’heure de date_ ou  _l’expression_ est ignoré. 
  
Si  _la date/_ heure est manquante ou ne peut pas être convertie en un résultat valide, cette fonction renvoie une #VALUE! erreur. 
  
La fonction TIMEVALUE accepte également une valeur de nombre unique pour  _l’expression_ où la partie décimale du résultat représente la fraction d’un jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

TIMEVALUE("6:00")
  
Renvoie la valeur représentant 06:00:00.
  
## <a name="example-2"></a>Exemple 2

TIMEVALUE("14:30") + 4 he.+ 30 me.
  
Renvoie la valeur représentant 19:00:00.
  
## <a name="example-3"></a>Exemple 3

TIMEVALUE("11 h, 1er juillet 1997")
  
Renvoie la valeur représentant 11:00:00.
  
## <a name="example-4"></a>Exemple 4

TIMEVALUE(0,6337)
  
Renvoie la valeur représentant 15:12:32.
  
## <a name="example-5"></a>Exemple 5

TIMEVALUE(« 7:89 »)
  
Renvoie une erreur #VALEUR!.
  

