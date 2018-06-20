---
title: ROUND, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arrondit un nombre selon la précision indiquée par l’argument nombredechiffres.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789506"
---
# <a name="round-function-visioshapesheet"></a>ROUND, fonction (VisioShapeSheet)

Arrondit un nombre selon la précision indiquée par *l’argument nombredechiffres* . 
  
## <a name="syntax"></a>Syntaxe

ROUND (** *numéro* **, ** *nombredechiffres* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir  <br/> |
| _nombredechiffres_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de décimales de précision  <br/> |
   
## <a name="remarks"></a>Remarques

Si le _nombredechiffres_ est supérieur à 0, _nombre_ est arrondi à _nombredechiffres_ à droite du séparateur décimal. Si le _nombredechiffres_ est 0, _nombre_ est arrondi à un entier. Si le _nombredechiffres_ est inférieur à 0, _nombre_ est arrondi à _nombredechiffres_ à gauche du séparateur décimal. 
  
## <a name="example-1"></a>Exemple 1

ROUND(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

ROUND(123.654,0)
  
Renvoie 124.
  
## <a name="example-3"></a>Exemple 3

ROUND(123.654,-1)
  
Renvoie 120.
  

