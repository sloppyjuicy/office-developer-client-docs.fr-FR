---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
ms.localizationpriority: medium
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arrondit un nombre à la précision représentée par numberofdigits .
ms.openlocfilehash: 6364599725a3bf7c3ebbb96044ac9c23b945d446
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780546"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Arrondit un nombre à la précision représentée par  *numberofdigits*  . 
  
## <a name="syntax"></a>Syntaxe

ROUND(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre à arrondir |
| _numberofdigits_ <br/> |Requis  <br/> |**Number** <br/> |Nombre de décimales de précision |
   
## <a name="remarks"></a>Remarques

Si  _numberofdigits_ est supérieur à  _0, le_ nombre est arrondi par  _nombreofdigits_ à droite de la décimale. Si  _numberofdigits est_ 0,  _le nombre_ est arrondi à un nombre complet. Si  _numberofdigits_ est inférieur à  _0, le_ nombre est arrondi par  _nombreofdigits_ à gauche de la décimale. 
  
## <a name="example-1"></a>Exemple 1

ROUND(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

ROUND(123.654,0)
  
Renvoie 124.
  
## <a name="example-3"></a>Exemple 3

ROUND(123,654,-1)
  
Renvoie 120.
  

