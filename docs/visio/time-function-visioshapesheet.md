---
title: TIME, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Renvoie l’heure en heure, minute et seconde.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789913"
---
# <a name="time-function-visioshapesheet"></a>TIME, fonction (VisioShapeSheet)

Renvoie l’heure en _heure_, _minute_et _seconde_.
  
## <a name="syntax"></a>Syntaxe

TEMPS (** *heure* **, ** *minute* **, ** *deuxième* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _heure_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant heure  <br/> |
| _minute_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant minute  <br/> |
| _seconde_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Composant seconde  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Numérique
  
## <a name="example-1"></a>Exemple 1

TIME(15;30;30)
  
Renvoie la valeur représentant 15:30:30.
  
## <a name="example-2"></a>Exemple 2

FORMAT(TIME(15;30;30),"HH:mm")
  
Renvoie la valeur représentant 15:30.
  
## <a name="example-3"></a>Exemple 3

TIME(15;30;30) + 8 he.
  
Renvoie la valeur représentant 23:30:30.
  

