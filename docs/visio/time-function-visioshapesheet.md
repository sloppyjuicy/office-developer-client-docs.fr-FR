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
description: Renvoie l’heure représentée par heure, minute et seconde.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414472"
---
# <a name="time-function-visioshapesheet"></a>TIME Function (VisioShapeSheet)

Renvoie l’heure représentée par  _l’heure,_  _la minute_ et la  _seconde_.
  
## <a name="syntax"></a>Syntaxe

TIME(** *hour* **, ** *minute* **, ** *second* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant heure  <br/> |
| _minute_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant minute  <br/> |
| _second_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant seconde  <br/> |
   
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
  

