---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Renvoie un integer, de 1 à 7, représentant le jour de la semaine dans l’heure ou l’expression.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404805"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY Function (VisioShapeSheet)

Renvoie un integer, de 1 à 7, représentant le jour de la semaine dans _l’heure ou_ l’expression . 
  
## <a name="syntax"></a>Syntaxe

WEEKDAY( » ** *datetime* ** « | ** *expression* ** [, ** *lcid* ** ]) 
  
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
  
Le résultat est compris entre lundi (1) et dimanche (7). Aucun arrondissement n’est effectué. Si  _la date/heure_ est manquante ou ne peut pas être interprétée comme une date ou une heure valide, la fonction renvoie une #VALUE! erreur. 
  
La fonction WEEKDAY accepte également une valeur de nombre unique pour  _l’expression_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

WEEKDAY("30 mai 1999")
  
Renvoie 7.
  
## <a name="example-2"></a>Exemple 2

WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)
  
Renvoie 2.
  
## <a name="example-3"></a>Exemple 3

WEEKDAY(35880.6337)
  
Renvoie 4.
  

