---
title: TIMEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Renvoie la valeur de temps représentée par dateheure ou expression, en fonction de la région et des paramètres de langue du système.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432323"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE Function (VisioShapeSheet)

Renvoie la valeur de temps représentée par _DateHeure_ ou _expression_, en fonction de la région et des paramètres de langue du système.
  
## <a name="syntax"></a>Syntaxe

TIMEVALUE ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _structure_ <br/> |Obligatoire  <br/> |**String** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Réelle** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
## <a name="remarks"></a>Remarques

Tout composant date dans _DateTime_ ou _expression_ est ignoré. 
  
Si l'argument _DateHeure_ est introuvable ou ne peut pas être converti en un résultat valide, cette fonction renvoie une #VALUE! «. 
  
La fonction TIMEVALUE accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

TIMEVALUE("6:00")
  
Renvoie la valeur représentant 06:00:00.
  
## <a name="example-2"></a>Exemple 2

TIMEVALUE("14:30") + 4 he.+ 30 me.
  
Renvoie la valeur représentant 19:00:00.
  
## <a name="example-3"></a>Exemple 3

TIMEVALUE("11 h, 1er juillet 1997")
  
Renvoie la valeur représentant 11:00:00.
  
## <a name="example-4"></a>Exemple 4

TIMEVALUE (0.6337)
  
Renvoie la valeur représentant 15:12:32.
  
## <a name="example-5"></a>Exemple 5

TIMEVALUE ("7:89")
  
Renvoie une erreur #VALEUR!.
  

