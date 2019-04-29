---
title: DAYOFYEAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Renvoie une valeur de type Integer, comprise entre 1 et 366, qui représente le jour séquentiel de l'année dans dateheure ou expression. La fonction DAYOFYEAR utilise le calendrier grégorien.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439450"
---
# <a name="dayofyear-function"></a>Fonction DAYOFYEAR

Renvoie une valeur de type Integer, comprise entre 1 et 366, qui représente le jour séquentiel de l'année dans _DateHeure_ ou _expression_. La fonction DAYOFYEAR utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DAYOFYEAR ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _structure_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Tous les composants d'heure dans _DateTime_ ou _expression_ ne sont pas pris en même temps. 
  
Le résultat est compris entre le 1er janvier et le 31 décembre. Aucun arrondissement n’est effectué. Si l'argument _DateHeure_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, la fonction renvoie une erreur. 
  
La fonction DAYOFYEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DAYOFYEAR("30 mai 1997 13:45:24")
  
Renvoie 150.
  
## <a name="example-2"></a>Exemple 2

DAYOFYEAR(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 157.
  
## <a name="example-3"></a>Exemple 3

DAYOFYEAR (35580.6337)
  
Renvoie 150.
  

