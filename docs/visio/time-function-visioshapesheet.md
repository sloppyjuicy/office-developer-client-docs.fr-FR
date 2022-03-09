---
title: TIME Function (VisioShapeSheet)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
ms.localizationpriority: medium
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Renvoie l’heure représentée par heure, minute et seconde.
ms.openlocfilehash: c961cf32a8d143652d18ac7501cd905c21d0d673
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404487"
---
# <a name="time-function-visioshapesheet"></a>TIME Function (VisioShapeSheet)

Renvoie l’heure représentée par _heure_, _minute_ et _seconde_.
  
## <a name="syntax"></a>Syntaxe

TIME(***hour** _, _*_minute_*_, _*_second_**)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Requis  <br/> |**Numérique** <br/> |Composant heure |
| _minute_ <br/> |Requis  <br/> |**Numérique** <br/> |Composant minute |
| _second_ <br/> |Requis  <br/> |**Numérique** <br/> |Composant seconde |

### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="example-1"></a>Exemple 1

TIME(15,30,30)
  
Renvoie la valeur représentant 15:30:30.
  
## <a name="example-2"></a>Exemple 2

FORMAT(TIME(15,30,30),"HH:mm »)
  
Renvoie la valeur représentant 15:30.
  
## <a name="example-3"></a>Exemple 3

TIME(15;30;30) + 8 he.
  
Renvoie la valeur représentant 23:30:30.
  