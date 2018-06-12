---
title: ISERRNA, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Renvoie la valeur TRUE si la valeur de cellreference est erreur type # n/a ! (non disponible) ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788864"
---
# <a name="iserrna-function"></a>ISERRNA, fonction

Renvoie la valeur TRUE si la valeur de _cellreference_ est erreur type # n/a ! (non disponible) ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERRNA (** *cellreference* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Cellule Scratch.A1  <br/> |="5 + 3"  <br/> |« 8 »  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |FALSE  <br/> |
   
Renvoie FALSE parce que la valeur renvoyée est disponible.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Cellule Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que la valeur renvoyée est du type d’erreur #N/A!
  

