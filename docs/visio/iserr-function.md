---
title: ISERR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
ms.localizationpriority: medium
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Renvoie TRUE si la valeur de cellreference est un type d’erreur à l’exception #N/A ; Sinon, elle renvoie FALSE. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: bb724fdb753ada86baf6cb421a2fa758620317ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612609"
---
# <a name="iserr-function"></a>Fonction ISERR

Renvoie TRUE si la valeur de  _cellreference_ est un type d’erreur à l’exception #N/A ; Sinon, elle renvoie FALSE. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
Renvoie FALSE parce que l’erreur #N/A! n’est pas reconnue par la fonction ISERR. Utilisez ISERROR pour trouver tous les types d’erreur.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House »  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERR.
  

