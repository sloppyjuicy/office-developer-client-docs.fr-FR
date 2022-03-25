---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, en tant que booléen, pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: c72c68d99491634ca40f36ccccffe14526309fe1
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406101"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate Cell (Page Properties Section)

Détermine si la page peut être dupliquée, en tant que booléen.
  
|Valeur |Description |
|:-----|:-----|
|TRUE  <br/> |**Le** doublon dans le menu de raccourci de page et la **méthode d’automatisation Page.Duplicate** sont tous deux désactivés pour la page. |
|FALSE  <br/> |La page peut être dupliquée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockDuplicate** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | PageLockDuplicate  <br/> |
   
Pour obtenir une référence à la **cellule PageLockDuplicate** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPage** <br/> |
| **Index de la cellule :**  <br/> |**visPageLockDuplicate** <br/> |
   

