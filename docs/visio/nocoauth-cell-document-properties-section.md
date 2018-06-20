---
title: NoCoauth, cellule (Section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Indique si un document stocké sur un serveur Microsoft SharePoint 2013 ou sur Microsoft OneDrive peut être modifié par plusieurs auteurs simultanément dans une session de co-création.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789171"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth, cellule (Section Document Properties)

Indique si un document stocké sur un serveur Microsoft SharePoint 2013 ou sur Microsoft OneDrive peut être modifié par plusieurs auteurs simultanément dans une session de co-création.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le document ne peut pas être attribué et est verrouillé pour modification lorsqu’il est ouvert.  <br/> |
|FALSE  <br/> |Le document peut être attribué.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | NoCoauth  <br/> |
   
Pour obtenir une référence à la cellule **NoCoauth** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocNoCoauth** <br/> |
   

