---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
ms.localizationpriority: medium
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Renvoie la valeur de date représentée par datetime ou expression.
ms.openlocfilehash: cd126f29baf1cf7731df3a2a57b0ec4d30a50ddf
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381067"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE Function (VisioShapeSheet)

Renvoie la valeur de date représentée par  _datetime_ ou  _expression_.
  
## <a name="syntax"></a>Syntaxe

DATEVALUE( » **_datetime_** « | **_expression_** [, **_lcid_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |

### <a name="return-value"></a>Valeur renvoyée

Datetime
  
## <a name="remarks"></a>Remarques

Les composants d’heure figurant dans les paramètres _datetime_ ou _expression_ ne sont pas pris en compte.
  
Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, DATEVALUE renvoie une erreur #VALEUR!.
  
La valeur renvoyée s’affiche au format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation.
  
La fonction DATEVALUE accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.
  
## <a name="example-1"></a>Exemple 1

DATEVALUE(NOW( )) + 5 je.
  
Renvoie la date actuelle augmentée de cinq jours.
  
## <a name="example-2"></a>Exemple 2

DATEVALUE(« 19/07/1995 12:30 »)
  
Renvoie la date.
  
## <a name="example-3"></a>Exemple 3

DATEVALUE("33 mai 1997")
  
Renvoie une erreur #VALEUR!.
  
## <a name="example-4"></a>Exemple 4

DATEVALUE(35580.6337)
  
Renvoie le 30/05/97.
  