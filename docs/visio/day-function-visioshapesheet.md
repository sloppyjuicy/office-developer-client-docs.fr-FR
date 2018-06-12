---
title: DAY, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Renvoie un entier, 1 et 31 représentant le jour de datetime ou expression. La fonction jour utilise le calendrier grégorien.
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788444"
---
# <a name="day-function-visioshapesheet"></a>DAY, fonction (VisioShapeSheet)

Renvoie un entier, 1 et 31 représentant le jour dans _dateheure_ ou _expression_. La fonction jour utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

JOUR (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
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
  
Aucun arrondi n’est effectué. Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, la fonction renvoie une erreur. 
  
La fonction DAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DAY("30 mai 1997 15:45:24")
  
Renvoie 30.
  
## <a name="example-2"></a>Exemple 2

DAY(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 6.
  
## <a name="example-3"></a>Exemple 3

DAY(35580.6337)
  
Renvoie 30.
  

