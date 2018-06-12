---
title: ISERR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Renvoie la valeur TRUE si la valeur de cellreference est une erreur à l’exception de # n/a ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788852"
---
# <a name="iserr-function"></a>ISERR, fonction

Renvoie la valeur TRUE si la valeur de _cellreference_ est une erreur à l’exception de # n/a ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

ISERR (** *cellreference* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Référence à une cellule  <br/> |
   
## <a name="example-1"></a>Exemple 1

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Cellule Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.a1)  <br/> |FALSE  <br/> |
   
Renvoie FALSE parce que l’erreur #N/A! n’est pas reconnue par la fonction ISERR. Utilisez ISERROR pour trouver tous les types d’erreur.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formula**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Maison"  <br/> |#VALEUR!  <br/> |
|Cellule Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERR.
  

