---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Définit si un document stocké sur un serveur Microsoft SharePoint 2013 ou un Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-édition.
ms.openlocfilehash: 829a51e33e0af5ca98ee898ee014f67cc453cd97
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775426"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Définit si un document stocké sur un serveur Microsoft SharePoint 2013 ou un Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-édition.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le document ne peut pas être co-écrit et est verrouillé pour modification à l’ouverture. |
|FALSE  <br/> |Le document peut être co-écrit. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | NoCoauth  <br/> |
   
Pour obtenir une référence à la **cellule NoCoauth** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocNoCoauth** <br/> |
   

