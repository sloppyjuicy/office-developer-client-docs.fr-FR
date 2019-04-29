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
description: Renvoie un entier compris entre 1 et 7, représentant le jour de la semaine dans dateheure ou expression.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404805"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY Function (VisioShapeSheet)

Renvoie un entier compris entre 1 et 7, représentant le jour de la semaine dans _DateHeure_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

WEEKDAY ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _structure_ <br/> |Obligatoire  <br/> |**String** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Réelle** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant heure de _DateTime_ ou _expression_ est ignoré. 
  
Le résultat est compris entre lundi (1) et dimanche (7). Aucun arrondissement n’est effectué. Si l'argument _DateHeure_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, la fonction renvoie une #VALUE! «. 
  
La fonction WEEKDAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

WEEKDAY("30 mai 1999")
  
Renvoie 7.
  
## <a name="example-2"></a>Exemple 2

WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)
  
Renvoie 2.
  
## <a name="example-3"></a>Exemple 3

JOUR DE LA SEMAINE (35880.6337)
  
Renvoie 4.
  

