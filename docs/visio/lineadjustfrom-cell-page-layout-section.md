---
title: LineAdjustFrom, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
ms.localizationpriority: medium
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.
ms.openlocfilehash: 1a9f7f823b73cd3ba77410f176f37326c2af6a33
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426369"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>LineAdjustFrom, cellule (section Page Layout)

Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.
  
|**Valeur**|**Ajustement**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Traits sans relation  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Tous les traits  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Aucun trait  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Style de positionnement par défaut  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineAdjustFrom par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LineAdjustFrom  <br/> |
   
Pour obtenir une référence à la cellule LineAdjustFrom à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
|**Index de la cellule :**  <br/> |**visPLOLineAdjustFrom** <br/> |
   

