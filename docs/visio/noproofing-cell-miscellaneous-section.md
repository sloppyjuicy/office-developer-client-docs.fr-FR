---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l'orthographe est corrigée automatiquement et si les fautes d'orthographe s'affichent pour la forme sélectionnée. Prend une valeur booléenne.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357224"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing Cell (Miscellaneous Section)

Détermine si l'orthographe est corrigée automatiquement et si les fautes d'orthographe s'affichent pour la forme sélectionnée. Prend une valeur **booléenne** . 
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L'orthographe n'est pas corrigée automatiquement et les fautes d'orthographe ne s'affichent pas pour la forme sélectionnée.  <br/> |
|FALSE  <br/> |L'orthographe est corrigée automatiquement et des fautes d'orthographe s'affichent pour la forme sélectionnée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule noProofing par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |NoProofing  <br/> |
   
Pour obtenir une référence à la cellule noProofing à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visObjNoProofing** <br/> |
   

