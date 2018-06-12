---
title: DATEVALUE, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Renvoie la valeur de date représentée par datetime ou expression.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788429"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE, fonction (VisioShapeSheet)

Renvoie la valeur de date représentée par _datetime_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

DATEVALUE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Datetime
  
## <a name="remarks"></a>Note

Les composants d’heure figurant dans *datetime* ou *expression* sont ignoré. 
  
Si *datetime* est introuvable ou ne peut pas être converti en un résultat valide, DATEVALUE renvoie une #VALUE ! erreur. 
  
La valeur renvoyée s’affiche au format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation. 
  
La fonction DATEVALUE accepte également une valeur numérique simple pour *expression* où la partie entière du résultat représente les jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DATEVALUE(NOW( )) + 5 je.
  
Renvoie la date actuelle augmentée de cinq jours.
  
## <a name="example-2"></a>Exemple 2

DATEVALUE("19/07/1995 12:30")
  
Renvoie la date.
  
## <a name="example-3"></a>Exemple 3

DATEVALUE("33 mai 1997")
  
Renvoie une erreur #VALEUR!.
  
## <a name="example-4"></a>Exemple 4

DATEVALUE(35580.6337)
  
Renvoie le 30/05/97.
  

