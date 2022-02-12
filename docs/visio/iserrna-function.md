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
ms.openlocfilehash: 2976bc61ee566410ef5f5254ed5085b98ab2e150
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775622"
---
# <a name="iserrna-function"></a>Fonction ISERRNA

Renvoie TRUE si la valeur de  _cellreference_ est de type erreur #N/A! (non disponible) ; Sinon, elle renvoie FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERRNA(** *cellreference* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Requis  <br/> |**String** <br/> |Référence à une cellule |
   
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
  

