---
title: ISERRVALUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Renvoie TRUE si la valeur de cellreference est erreur type #VALUE, où un argument dans la formule est de type incorrect. La fonction ISERRVALUE est utilisée dans les expressions logiques qui font référence à une autre cellule.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788869"
---
# <a name="iserrvalue-function"></a>ISERRVALUE, fonction

Renvoie TRUE si la valeur de _cellreference_ est erreur type #VALUE, où un argument dans la formule est de type incorrect. La fonction ISERRVALUE est utilisée dans les expressions logiques qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERRVALUE (** *cellreference* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Référence à une cellule  <br/> |
   
## <a name="remarks"></a>Note

Les cellules Montage de A à D ne renvoient pas l’erreur #VALEUR! parce que la formule peut contenir des nombres et des lettres dans une même chaîne. Toutefois, les cellules X et Y ne doivent contenir que des nombres. 
  
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Maison"  <br/> |#VALEUR!  <br/> |
|Cellule Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Renvoie 2 parce que la valeur renvoyée est une erreur #VALEUR! et l’expression demande à Microsoft Visio de renvoyer un 2 à la place de l’erreur.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Cellule Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Renvoie 12 parce que la valeur renvoyée n’est pas une erreur #VALEUR! et l’expression demande à Visio de renvoyer la valeur de la cellule d’origine.
  

