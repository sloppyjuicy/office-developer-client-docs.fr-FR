---
title: UIVisibility, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789988"
---
# <a name="uivisibility-cell-page-properties-section"></a>UIVisibility, cellule (section Page Properties)

Détermine si le nom de la page est exposé dans l'interface utilisateur (IU).
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Affiche le nom de la page dans l'IU (par défaut).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |N'affiche pas le nom de la page dans l'IU.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Remarques

Définir la cellule UIVisibility sur **visUIVHidden** empêche la page d’apparaître n’importe où dans l’interface utilisateur où la chaîne contenant le nom de la page s’affiche. Par exemple, la page ne serait pas figurer en tant qu’option dans l' **Explorateur de dessins** ou sur les onglets de page. La page reste accessible, toutefois, si vous utilisez des chemins d’accès Automation ou l’interface utilisateur qui n’incluent pas le nom de la page, par exemple, la commande **Imprimer** . 
  
 Cette cellule est destinée aux pages du document ; Il n’est pas destiné à utiliser avec les pages de superposition de balisage, dont la cellule UIVisibility sur **visUIVHidden** la valeur par défaut et ne doit pas être modifiée. 
  
> [!NOTE]
> Pour masquer une page à partir de la commande **d’impression** du document, faites-en une page d’arrière-plan (la propriété**Type** est **visTypeBackground** ) qui n’est pas utilisé en tant qu’arrière-plan par n’importe quelle page (les formes sur les pages d’arrière-plan sont imprimées lorsqu’une page à l’utiliser en tant qu’arrière-plan est impression). Commande **d’impression** du document ne fonctionne qu’avec des pages indexées et les pages d’arrière-plan ne sont pas indexés. 
  
Pour obtenir une référence à la cellule UIVisibility par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |UIVisibility  <br/> |
   
Pour obtenir une référence à la cellule UIVisibility par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageUIVisibility** <br/> |
   

