---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Renvoie TRUE si la valeur de cellreference est un type d’erreur ; Sinon, elle renvoie FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421542"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR Function (VisioShapeSheet)

Renvoie TRUE si la valeur de  _cellreference_ est un type d’erreur ; Sinon, elle renvoie FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERROR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.A1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que l’erreur #N/A! est reconnue par la fonction ISERROR. Vous pouvez utiliser ISERR pour trouver tous les types d’erreur à l’exception de l’erreur #N/A!.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House »  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERROR. Pour élaborer une expression basée sur l’erreur #VALEUR!, utilisez la fonction ISERRVALUE.
  

