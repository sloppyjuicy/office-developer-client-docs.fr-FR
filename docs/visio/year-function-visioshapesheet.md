---
title: YEAR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Renvoie un entier qui représente l’année grégorien dans l’heure ou l’expression date/heure, mise en forme selon le style de date courte définie par les paramètres de région et de langue actuels du système.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420709"
---
# <a name="year-function-visioshapesheet"></a>YEAR Function (VisioShapeSheet)

Renvoie un entier qui représente l’année grégorien dans l’heure ou _l’expression date/heure,_ mise en forme selon le style de date courte définie par les paramètres de région et de langue actuels du système. 
  
## <a name="syntax"></a>Syntaxe

YEAR( » ** *datetime* ** « | ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatoire  <br/> |**String** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si  _la date/heure_ est manquante ou ne peut pas être interprétée comme une date ou une heure valide, YEAR renvoie une erreur. 
  
La fonction YEAR accepte également une valeur de nombre unique pour  _l’expression,_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

YEAR(« 27/10/2007 13:45:24 »)
  
Renvoie 2007.
  
## <a name="example-2"></a>Exemple 2

YEAR(VALEURDATE("25 déc. 2006") + 7 je.)
  
Renvoie 2007.
  
## <a name="example-3"></a>Exemple 3

YEAR(35580.6337)
  
Renvoie 1997.
  

