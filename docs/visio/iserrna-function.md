---
title: ISERRNA, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
ms.localizationpriority: medium
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Renvoie TRUE si la valeur de cellreference est de type erreur #N/A! (non disponible) ; Sinon, elle renvoie FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: ad39cc4fb96600f90ff24673e591fbc409ae4d77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612595"
---
# <a name="iserrna-function"></a>Fonction ISERRNA

Renvoie TRUE si la valeur de  _cellreference_ est de type erreur #N/A! (non disponible) ; Sinon, elle renvoie FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERRNA(** *cellreference* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |FALSE  <br/> |
   
Renvoie FALSE parce que la valeur renvoyée est disponible.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que la valeur renvoyée est du type d’erreur #N/A!
  

