---
title: PreviewQuality, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789330"
---
# <a name="previewquality-cell-document-properties-section"></a>PreviewQuality, cellule (section Document Properties)

Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.
  
|**Valeur**|**Qualité d’aperçu**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Brouillon  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Détaillé  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sur l’onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur le bouton **Office** , cliquez sur l’onglet **Infos** , cliquez sur **Propriétés du Document**, puis cliquez sur **Propriétés avancées**).
  
Pour obtenir une référence à la cellule PreviewQuality par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PreviewQuality  <br/> |
   
Pour obtenir une référence à la cellule PreviewQuality par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocPreviewQuality** <br/> |
   

