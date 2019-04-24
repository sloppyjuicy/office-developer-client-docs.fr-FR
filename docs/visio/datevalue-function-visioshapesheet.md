---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Renvoie la valeur de date représentée par DateTime ou expression.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360311"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE Function (VisioShapeSheet)

Renvoie la valeur de date représentée par _DateTime_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

DATEVALUE ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _structure_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Structure
  
## <a name="remarks"></a>Remarques

Tous les composants d'heure dans *DateTime* ou *expression* ne sont pas pris en même temps. 
  
Si l'argument *DateHeure* est introuvable ou ne peut pas être converti en un résultat valide, la fonction DateValue renvoie une #VALUE! «. 
  
La valeur renvoyée s’affiche au format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation. 
  
La fonction DATEVALUE accepte également une valeur numérique simple pour *expression* où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DATEVALUE(NOW( )) + 5 je.
  
Renvoie la date actuelle augmentée de cinq jours.
  
## <a name="example-2"></a>Exemple 2

DATEVALUE ("7/19/1995 12:30")
  
Renvoie la date.
  
## <a name="example-3"></a>Exemple 3

DATEVALUE("33 mai 1997")
  
Renvoie une erreur #VALEUR!.
  
## <a name="example-4"></a>Exemple 4

DATEVALUE (35580.6337)
  
Renvoie le 30/05/97.
  

