---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l’orthographe est corrigée automatiquement et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Prend une valeur boolé américaine.
ms.openlocfilehash: 6e4ffc00e9d45c808655363619a5331030cb84a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573830"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing Cell (Miscellaneous Section)

Détermine si l’orthographe est corrigée automatiquement et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Prend une **valeur boolé** américaine. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L’orthographe n’est pas corrigée automatiquement et les fautes d’orthographe ne s’affichent pas pour la forme sélectionnée.  <br/> |
|FALSE  <br/> |L’orthographe est automatiquement corrigée et les fautes d’orthographe s’affichent pour la forme sélectionnée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoProofing par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |NoProofing  <br/> |
   
Pour obtenir une référence à la cellule NoProofing à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visObjNoProofing** <br/> |
   

