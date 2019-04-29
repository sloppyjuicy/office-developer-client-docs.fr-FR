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
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416817"
---
# <a name="previewquality-cell-document-properties-section"></a>PreviewQuality, cellule (section Document Properties)

Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.
  
|**Valeur**|**Qualité d'aperçu**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Première version  <br/> |**visDocPreviewQualityDraft** <br/> |
| 0,1  <br/> | Précises  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sous l'onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur le bouton **Office** , cliquez sur l'onglet **informations** , cliquez sur **Propriétés du document**, puis cliquez sur **Propriétés avancées**).
  
Pour obtenir une référence à la cellule PreviewQuality par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PreviewQuality  <br/> |
   
Pour obtenir une référence à la cellule PreviewQuality à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocPreviewQuality** <br/> |
   

