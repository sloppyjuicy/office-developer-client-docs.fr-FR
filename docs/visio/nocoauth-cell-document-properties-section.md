---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Définit si un document stocké sur un serveur ou un Microsoft OneDrive Microsoft SharePoint 2013 peut être modifié simultanément par plusieurs auteurs au cours d’une session de co-édition.
ms.openlocfilehash: 3e7eccbc983464ca7de747d8254cf1075c966e96
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633861"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Définit si un document stocké sur un serveur ou un Microsoft OneDrive Microsoft SharePoint 2013 peut être modifié simultanément par plusieurs auteurs au cours d’une session de co-édition.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le document ne peut pas être co-écrit et est verrouillé pour modification à l’ouverture. |
|FALSE  <br/> |Le document peut être co-écrit. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | NoCoauth  <br/> |
   
Pour obtenir une référence à la **cellule NoCoauth** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowDoc** <br/> |
| **Index de la cellule :**  <br/> |**visDocNoCoauth** <br/> |
   

