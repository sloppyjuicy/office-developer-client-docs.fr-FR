---
title: NoProofing, cellule (Section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l’orthographe a été corrigé automatiquement, et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Accepte une valeur booléenne.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19789170"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing, cellule (Section Miscellaneous)

Détermine si l’orthographe a été corrigé automatiquement, et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Accepte une valeur **booléenne** . 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Orthographe n’est pas corrigé automatiquement et les fautes d’orthographe ne sont pas affichées de la forme sélectionnée.  <br/> |
|FALSE  <br/> |Corrigé l’orthographe et les fautes d’orthographe sont affichés de la forme sélectionnée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoProofing par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |NoProofing  <br/> |
   
Pour obtenir une référence à la cellule NoProofing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visObjNoProofing** <br/> |
   

