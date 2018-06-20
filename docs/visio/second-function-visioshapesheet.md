---
title: DEUXIÈME fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Renvoie un entier, 0 et 59, représentant le composant secondes de datetime ou expression.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789600"
---
# <a name="second-function-visioshapesheet"></a>DEUXIÈME fonction (VisioShapeSheet)

Renvoie un entier, 0 et 59, représentant le composant secondes de _datetime_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

DEUXIÈME (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Numérique** <br/> |L’identificateur de paramètres régionaux à utiliser lors de l’évaluation non locaux _datetime_. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Le composant date de _datetime_ ou _expression_ est ignoré. 
  
Aucun arrondi n’est effectué. Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, cette fonction renvoie une erreur. 
  
La fonction SECOND accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

SECOND("30/05/1997 13:45:32")
  
Renvoie 32.
  
## <a name="example-2"></a>Exemple 2

SECOND(TIMEVALUE("30 mai 1996 12:07:45") + 7 se.)
  
Renvoie 52.
  
## <a name="example-3"></a>Exemple 3

SECOND(0.6337)
  
Renvoie 32.
  

