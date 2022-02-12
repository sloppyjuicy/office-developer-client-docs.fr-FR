---
title: TRUNC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
ms.localizationpriority: medium
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Renvoie un nombre tronqué au nombre de chiffres spécifié.
ms.openlocfilehash: ec823efa40f8baef0000c4b719c76198dd402b3a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777977"
---
# <a name="trunc-function"></a>Fonction TRUNC

Renvoie un nombre tronqué au nombre de chiffres spécifié.
  
## <a name="syntax"></a>Syntaxe

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Numérique** <br/> |Nombre à tronquer. |
| _numberofdigits_ <br/> |Requis  <br/> |**Numérique** <br/> |Nombre de chiffres à _tronqué._ |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique.
  
## <a name="remarks"></a>Remarques

Si  _numberofdigits_ est supérieur à  _0, le_ nombre est tronqué en  _nombreofdigits_ à droite de la décimale. Si  _le nombreofdigits_ est 0,  _le_ nombre est tronqué à un nombre total. Si  _numberofdigits_ est inférieur à  _0, le_ nombre est tronqué en  _nombreofdigits_ à gauche de la décimale. 
  
## <a name="example-1"></a>Exemple 1

TRUNC(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

TRUNC(123.654,0)
  
Renvoie 123.
  
## <a name="example-3"></a>Exemple 3

TRUNC(123.654,-1)
  
Renvoie 120.
  

