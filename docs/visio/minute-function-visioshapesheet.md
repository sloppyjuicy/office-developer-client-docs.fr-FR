---
title: Fonction MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Renvoie un entier compris entre 0 et 59 représentant le composant des minutes de datetime ou expression.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789151"
---
# <a name="minute-function-visioshapesheet"></a>Fonction MINUTE (VisioShapeSheet)

Renvoie un entier compris entre 0 et 59 représentant le composant des minutes de *datetime* ou *expression* . 
  
## <a name="syntax"></a>Syntaxe

MINUTE (« *datetime* » |  *expression*  [, *lcid* ]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Le composant date de _datetime_ et _expression_ est ignoré. 
  
Aucun arrondi n’est effectué. Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, la fonction renvoie une erreur. 
  
La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation.
  
La fonction MINUTE accepte également une valeur numérique simple pour _expression_ où la partie décimale représente la fraction du jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

MINUTE("07/07/1999 13:45:24")
  
Renvoie 45.
  
## <a name="example-2"></a>Exemple 2

MINUTE(VALEURHEURE("25 janv. 1999 12:07:45") + 6 me.)
  
Renvoie 13.
  
## <a name="example-3"></a>Exemple 3

MINUTE(0.575)
  
Renvoie 48.
  

