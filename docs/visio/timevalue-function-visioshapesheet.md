---
title: TimeValue, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Renvoie la valeur d’heure représentée par dateheure ou expression, selon régionales votre système et linguistiques paramètres.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789899"
---
# <a name="timevalue-function-visioshapesheet"></a>TimeValue, fonction (VisioShapeSheet)

Renvoie la valeur d’heure représentée par les _paramètres datetime_ ou _expression_, selon régionales votre système et linguistiques paramètres.
  
## <a name="syntax"></a>Syntaxe

TIMEVALUE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
## <a name="remarks"></a>Note

Le composant date de _datetime_ ou _expression_ est ignoré. 
  
Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, cette fonction renvoie une #VALUE ! erreur. 
  
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

TIMEVALUE(0.6337)
  
Renvoie la valeur représentant 15:12:32.
  
## <a name="example-5"></a>Exemple 5

TIMEVALUE("7:89")
  
Renvoie une erreur #VALEUR!.
  

