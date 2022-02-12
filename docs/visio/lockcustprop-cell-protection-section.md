---
title: LockCustProp, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
ms.localizationpriority: medium
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Détermine si l’utilisateur peut ajouter, supprimer ou modifier des données de forme dans l’interface utilisateur à l’aide de la boîte de dialogue Définir les données de forme ou du menu contextuel de la fenêtre Données de forme.
ms.openlocfilehash: b5630f8400ceab7ccf038cbae27e3126f315dadf
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780658"
---
# <a name="lockcustprop-cell-protection-section"></a>LockCustProp, cellule (section Protection)

Détermine si l’utilisateur peut ajouter, supprimer ou modifier des données de forme dans l’interface utilisateur à l’aide de la boîte de dialogue **Définir les données de forme** ou du menu contextuel de la fenêtre **Données de forme**. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La commande **Définir les données de forme** dans le menu contextuel de la fenêtre **Données de forme** est désactivée. |
|FALSE  <br/> |La commande **Définir les données de forme** dans le menu contextuel de la fenêtre **Données de forme** est activée (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

La valeur TRUE n'empêche pas un utilisateur de changer la valeur d'un élément de données de forme ni de modifier la section Données de forme de la fenêtre Feuille ShapeSheet. 
  
Pour obtenir une référence à la cellule LockCustProp par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |LockCustProp  <br/> |
   
Pour obtenir une référence à la cellule LockCustProp à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockCustProp** <br/> |
   

