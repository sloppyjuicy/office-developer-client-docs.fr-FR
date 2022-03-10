---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l’orthographe est corrigée automatiquement et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Prend une valeur boolé américaine.
ms.openlocfilehash: 37ff7ff92b434cd2356e0ffed72670cf1da88fc0
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426957"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing Cell (Miscellaneous Section)

Détermine si l’orthographe est corrigée automatiquement et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Prend une **valeur boolé** américaine. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L’orthographe n’est pas corrigée automatiquement et les fautes d’orthographe ne sont pas affichées pour la forme sélectionnée. |
|FALSE  <br/> |L’orthographe est automatiquement corrigée et les fautes d’orthographe sont affichées pour la forme sélectionnée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoProofing par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |NoProofing  <br/> |
   
Pour obtenir une référence à la cellule NoProofing à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowMisc** <br/> |
|**Index de la cellule :**  <br/> |**visObjNoProofing** <br/> |
   

