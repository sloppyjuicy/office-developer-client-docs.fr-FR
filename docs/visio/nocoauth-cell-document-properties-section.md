---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Définit si un document stocké sur un serveur microsoft SharePoint 2013 ou un Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-édition.
ms.openlocfilehash: 505617992f2a35e0603ed676b1e6dcb1fa1b5511
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562971"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Définit si un document stocké sur un serveur microsoft SharePoint 2013 ou un Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-édition.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le document ne peut pas être co-écrit et est verrouillé pour modification à l’ouverture.  <br/> |
|FALSE  <br/> |Le document peut être co-écrit.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | NoCoauth  <br/> |
   
Pour obtenir une référence à la **cellule NoCoauth** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocNoCoauth** <br/> |
   

