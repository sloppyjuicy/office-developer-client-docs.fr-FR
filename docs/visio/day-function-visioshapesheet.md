---
title: DAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Renvoie un entier compris entre 1 et 31, représentant le jour dans dateheure ou expression. La fonction DAY utilise le calendrier grégorien.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360295"
---
# <a name="day-function-visioshapesheet"></a>DAY Function (VisioShapeSheet)

Renvoie un entier compris entre 1 et 31, représentant le jour dans _DateHeure_ ou _expression_. La fonction DAY utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DAY ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
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
  
Aucun arrondissement n’est effectué. Si l'argument _DateHeure_ est introuvable ou ne peut pas être converti en un résultat valide, la fonction renvoie une erreur. 
  
La fonction DAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DAY("30 mai 1997 15:45:24")
  
Renvoie 30.
  
## <a name="example-2"></a>Exemple 2

DAY(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 6.
  
## <a name="example-3"></a>Exemple 3

JOUR (35580.6337)
  
Renvoie 30.
  

