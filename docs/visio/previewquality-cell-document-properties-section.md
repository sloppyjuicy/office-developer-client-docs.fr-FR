---
title: PreviewQuality, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
ms.localizationpriority: medium
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.
ms.openlocfilehash: bca9044f05be945d62d4c769dcb5835205871307
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626177"
---
# <a name="previewquality-cell-document-properties-section"></a>PreviewQuality, cellule (section Document Properties)

Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.
  
|**Valeur**|**Qualité d'aperçu**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Brouillon  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Détails  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sous l’onglet Résumé dans la  boîte de dialogue Propriétés (cliquez sur le bouton **Office**, sur l’onglet Informations, sur Propriétés du **document**, puis sur Propriétés  **avancées).**
  
Pour obtenir une référence à la cellule PreviewQuality par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | PreviewQuality  <br/> |
   
Pour obtenir une référence à la cellule PreviewQuality à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowDoc** <br/> |
| **Index de la cellule :**  <br/> |**visDocPreviewQuality** <br/> |
   

