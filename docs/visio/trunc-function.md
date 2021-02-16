---
title: TRUNC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Renvoie un nombre tronqué au nombre de chiffres spécifié.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426498"
---
# <a name="trunc-function"></a>Fonction TRUNC

Renvoie un nombre tronqué au nombre de chiffres spécifié.
  
## <a name="syntax"></a>Syntaxe

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre à tronquer.  <br/> |
| _numberofdigits_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre de chiffres à _tronqué._  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique.
  
## <a name="remarks"></a>Remarques

Si  _numberofdigits_ est supérieur à  _0,_ le nombre est tronqué en  _nombreofdigits_ à droite de la décimale. Si  _le nombreofdigits_ est 0,  _le_ nombre est tronqué à un nombre total. Si _numberofdigits_ est inférieur à  0, le nombre est tronqué en _nombreofdigits_ à gauche de la décimale. 
  
## <a name="example-1"></a>Exemple 1

TRUNC(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

TRUNC(123.654,0)
  
Renvoie 123.
  
## <a name="example-3"></a>Exemple 3

TRUNC(123.654,-1)
  
Renvoie 120.
  

