---
title: ISERRVALUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
ms.localizationpriority: medium
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Renvoie TRUE si la valeur de cellreference est de type #VALUE, où un argument dans la formule est du type erroné. La fonction ISERRVALUE est utilisée dans les expressions logiques qui font référence à une autre cellule.'
ms.openlocfilehash: 509ed277070babc54a0b2c05430a328581e3bc77
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775587"
---
# <a name="iserrvalue-function"></a>Fonction ISERRVALUE

Renvoie TRUE si la valeur de  _cellreference_ est de type #VALUE, où un argument dans la formule est du type erroné. La fonction ISERRVALUE est utilisée dans les expressions logiques qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERRVALUE(** *cellreference* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Requis  <br/> |**String** <br/> |Référence à une cellule |
   
## <a name="remarks"></a>Remarques

Les cellules Montage de A à D ne renvoient pas l’erreur #VALEUR! parce que la formule peut contenir des nombres et des lettres dans une même chaîne. Toutefois, les cellules X et Y ne doivent contenir que des nombres. 
  
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Maison"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Renvoie 2 parce que la valeur renvoyée est une erreur #VALEUR! et l’expression demande à Microsoft Visio de renvoyer un 2 à la place de l’erreur.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Renvoie 12 parce que la valeur renvoyée n’est pas une erreur #VALEUR! et l’expression demande à Visio de renvoyer la valeur de la cellule d’origine.
  

