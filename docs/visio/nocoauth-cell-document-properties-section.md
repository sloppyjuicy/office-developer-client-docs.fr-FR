---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Définit si un document stocké sur un serveur Microsoft SharePoint 2013 ou Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-création.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319438"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Définit si un document stocké sur un serveur Microsoft SharePoint 2013 ou Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-création.
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le document ne peut pas être co-créé et ne peut pas être modifié lorsqu'il est ouvert.  <br/> |
|FALSE  <br/> |Le document peut être co-créé.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | NoCoauth  <br/> |
   
Pour obtenir une référence à la cellule **NoCoauth** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocNoCoauth** <br/> |
   

