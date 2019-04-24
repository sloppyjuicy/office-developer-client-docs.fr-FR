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
description: Renvoie un entier compris entre 0 et 59, qui représente le composant secondes de DateTime ou expression.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332787"
---
# <a name="second-function-visioshapesheet"></a>SECOND Function (VisioShapeSheet)

Renvoie un entier compris entre 0 et 59, qui représente le composant secondes de _DateTime_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

SECOND ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _structure_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser lors de l'évaluation d'un _DateTime_non local. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant date dans _DateTime_ ou _expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si l'argument _DateHeure_ est introuvable ou ne peut pas être converti en un résultat valide, une erreur est renvoyée. 
  
La fonction SECOND accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

SECONDE ("05/30/1997 13:45:32")
  
Renvoie 32.
  
## <a name="example-2"></a>Exemple 2

SECOND(TIMEVALUE("30 mai 1996 12:07:45") + 7 se.)
  
Renvoie 52.
  
## <a name="example-3"></a>Exemple 3

SECONDE (0.6337)
  
Renvoie 32.
  

