---
title: UIVisibility, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
ms.localizationpriority: medium
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).
ms.openlocfilehash: 38b667739df13656872d6ffce235c29e6e796342
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779013"
---
# <a name="uivisibility-cell-page-properties-section"></a>UIVisibility, cellule (section Page Properties)

Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Affiche le nom de la page dans l'IU (par défaut). |**visUIVNormal** <br/> |
|1  <br/> |N'affiche pas le nom de la page dans l'IU. |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Remarques

Définir la cellule UIVisibility sur **visUIVHidden** empêche la page d’apparaître n’importe où dans l’interface utilisateur où la chaîne contenant le nom de la page apparaît. Par exemple, la page ne serait pas présentée comme option dans l’**Explorateur de dessin** ou dans les onglets de page. La page reste toutefois accessible si vous utilisez Automation ou des chemins d’accès d’interface utilisateur qui n’incluent pas le nom de la page, par exemple, la **commande Imprimer** . 
  
 Cette cellule est destinée à être utilisée uniquement avec des pages de document  elle n'est pas destinée à être utilisée avec des pages de superposition de marque de révision, dont la cellule UIVisibility est définie par défaut sur **visUIVHidden** et ne doit pas être modifiée. 
  
> [!NOTE]
> Pour masquer une page de la commande Imprimer du  document, faites-en une page d’arrière-plan (la propriété **Type** est **visTypeBackground**) qui n’est utilisée comme arrière-plan par aucune page (les formes des pages d’arrière-plan sont imprimées lorsqu’une page l’utilise en arrière-plan). La commande **Imprimer du document** fonctionne uniquement avec les pages indexées et les pages d’arrière-plan ne sont pas indexées. 
  
Pour obtenir une référence à la cellule UIVisibility par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |UIVisibility  <br/> |
   
Pour obtenir une référence à la cellule UIVisibility à l'aide d'un index à partir un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageUIVisibility** <br/> |
   

