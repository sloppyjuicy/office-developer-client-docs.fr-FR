---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
ms.localizationpriority: medium
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Renvoie l’heure représentée par heure, minute et seconde.
ms.openlocfilehash: 931e52a5b344c20ffcc51815a34d9d244cf07933
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778054"
---
# <a name="time-function-visioshapesheet"></a>TIME Function (VisioShapeSheet)

Renvoie l’heure représentée par  _heure_,  _minute_ et  _seconde_.
  
## <a name="syntax"></a>Syntaxe

TIME(** *hour* **, ** *minute* **, ** *second* ** ) 
  
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
  

