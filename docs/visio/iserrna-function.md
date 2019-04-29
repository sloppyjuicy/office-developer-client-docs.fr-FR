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
description: "Renvoie TRUE si la valeur de cellreference est un type d'erreur #N/A! (non disponible); dans le cas contraire, elle renvoie la valeur FALSe. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule."
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432113"
---
# <a name="iserrna-function"></a>Fonction ISERRNA

Renvoie TRUE si la valeur de _cellreference_ est un type d'erreur #N/a! (non disponible); dans le cas contraire, elle renvoie la valeur FALSe. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERRNA (* * *cellreference* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cellule**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 3"  <br/> |8bits  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |FALSE  <br/> |
   
Renvoie FALSE parce que la valeur renvoyée est disponible.
  
## <a name="example-2"></a>Exemple 2

|**Cellule**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que la valeur renvoyée est du type d’erreur #N/A!
  

