---
title: IsError, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Renvoie la valeur TRUE si la valeur de cellreference est une erreur ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788866"
---
# <a name="iserror-function-visioshapesheet"></a>IsError, fonction (VisioShapeSheet)

Renvoie la valeur TRUE si la valeur de _cellreference_ est une erreur ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERROR (** *cellreference* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Cellule Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.a1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que l’erreur #N/A! est reconnue par la fonction ISERROR. Vous pouvez utiliser ISERR pour trouver tous les types d’erreur à l’exception de l’erreur #N/A!.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Maison"  <br/> |#VALEUR!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.X1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERROR. Pour élaborer une expression basée sur l’erreur #VALEUR!, utilisez la fonction ISERRVALUE.
  

