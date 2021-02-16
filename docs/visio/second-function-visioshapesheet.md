---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Renvoie un nombre integer, de 0 à 59, qui représente le composant de secondes de date/heure ou d’expression.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404875"
---
# <a name="second-function-visioshapesheet"></a>SECOND Function (VisioShapeSheet)

Renvoie un nombre integer, de 0 à 59, qui représente le composant de secondes de  _date/heure_ ou  _d’expression_.
  
## <a name="syntax"></a>Syntaxe

SECOND( » ** *datetime* ** « | ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une  _date/heure_ non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant date dans  _l’heure de date_  _ou l’expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si  _la date/heure_ est manquante ou ne peut pas être convertie en un résultat valide, cette fonction renvoie une erreur. 
  
La fonction SECOND accepte également une valeur de nombre unique pour  _l’expression_ où la partie décimale du résultat représente la fraction d’un jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

SECOND(« 30/05/1997 13:45:32 »)
  
Renvoie 32.
  
## <a name="example-2"></a>Exemple 2

SECOND(TIMEVALUE("30 mai 1996 12:07:45") + 7 se.)
  
Renvoie 52.
  
## <a name="example-3"></a>Exemple 3

SECOND(0,6337)
  
Renvoie 32.
  

