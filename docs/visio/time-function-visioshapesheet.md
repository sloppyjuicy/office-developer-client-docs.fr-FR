---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Renvoie l'heure représentée par les heures, les minutes et les secondes.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280996"
---
# <a name="time-function-visioshapesheet"></a>TIME Function (VisioShapeSheet)

Renvoie l'heure représentée par les _heures_, les _minutes_et les _secondes_.
  
## <a name="syntax"></a>Syntaxe

HEURE (* * *heure* * *, * * *minute* * *, * * *seconde* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _h/24_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant heure  <br/> |
| _précédente_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant minute  <br/> |
| _seconde_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant seconde  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="example-1"></a>Exemple 1

HEURE (15, 30, 30)
  
Renvoie la valeur représentant 15:30:30.
  
## <a name="example-2"></a>Exemple 2

FORMAT (durée (15, 30, 30), "HH: mm")
  
Renvoie la valeur représentant 15:30.
  
## <a name="example-3"></a>Exemple 3

TIME(15;30;30) + 8 he.
  
Renvoie la valeur représentant 23:30:30.
  

