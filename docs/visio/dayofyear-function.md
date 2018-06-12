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
description: Renvoie un entier, de 1 à 366 qui représente le jour de l’année de datetime ou expression. La fonction DAYOFYEAR utilise le calendrier grégorien.
ms.openlocfilehash: 2fd80a2554c268d276deaa524a9d98eebc6a48d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788454"
---
# <a name="dayofyear-function"></a>DAYOFYEAR, fonction

Renvoie un entier, de 1 à 366 qui représente le jour de l’année dans les _paramètres datetime_ ou _expression_. La fonction DAYOFYEAR utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DAYOFYEAR (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Les composants d’heure figurant dans _datetime_ ou _expression_ sont ignoré. 
  
Le résultat correspond au 1er janvier au 31 décembre. Aucun arrondi n’est effectué. Si _datetime_ est introuvable ou ne peut pas être interprété comme une date ou heure valide, la fonction renvoie une erreur. 
  
La fonction DAYOFYEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DAYOFYEAR("30 mai 1997 13:45:24")
  
Renvoie 150.
  
## <a name="example-2"></a>Exemple 2

DAYOFYEAR(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 157.
  
## <a name="example-3"></a>Exemple 3

DAYOFYEAR(35580.6337)
  
Renvoie 150.
  

