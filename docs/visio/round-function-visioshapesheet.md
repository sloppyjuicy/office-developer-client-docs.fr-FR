---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arrondit un nombre à la précision représentée par le NombreDeChiffres.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439967"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Arrondit un nombre à la précision représentée par le *NombreDeChiffres* . 
  
## <a name="syntax"></a>Syntaxe

ROUND (* * *nombre* * *, * * *NombreDeChiffres* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir  <br/> |
| _NombreDeChiffres_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de décimales de précision  <br/> |
   
## <a name="remarks"></a>Remarques

Si le _NombreDeChiffres_ est supérieur à 0, le _nombre_ est arrondi par le _NombreDeChiffres_ à droite du séparateur décimal. Si le _NombreDeChiffres_ est 0, le _nombre_ est arrondi à un entier. Si le _NombreDeChiffres_ est inférieur à 0, le _nombre_ est arrondi par le _NombreDeChiffres_ à gauche du séparateur décimal. 
  
## <a name="example-1"></a>Exemple 1

ROUND (123.654, 2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

ROUND (123.654, 0)
  
Renvoie 124.
  
## <a name="example-3"></a>Exemple 3

ROUND (123.654,-1)
  
Renvoie 120.
  

