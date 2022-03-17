---
title: Bullet, cellule (section Paragraph)
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
ms.localizationpriority: medium
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Détermine le style de puce.
ms.openlocfilehash: 19ee2e8912db7d1acf0e8c7ac36648b965355c70
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519866"
---
# <a name="bullet-cell-paragraph-section"></a>Bullet, cellule (section Paragraph)

Détermine le style de puce.
  
|**Valeur**|**Style de puce**|
|:-----|:-----|
|0   |Aucun |
|1   |![puce arrondie](media/IC_Bullet1_ZA07645847.gif) |
|2   |![puces en losange](media/IC_Bullet2_ZA07645848.gif) |
|3   |![puce carrée](media/IC_Bullet3_ZA07645849.gif) |
|4   |![puce case à cocher](media/IC_Bullet4_ZA07645851.gif) |
|5   |![puces à quatre losanges](media/IC_Bullet5_ZA07645852.gif) |
|6    |![puce de flèche de procédure](media/IC_Bullet6_ZA07645853.gif) |
|7    |![coche de puce](media/IC_Bullet7_ZA07645854.gif) |

 
## <a name="remarks"></a>Remarques

Pour définir la valeur de cette cellule, cliquez avec le bouton droit sur une forme, pointez sur **Format**, cliquez sur **Texte**, puis cliquez sur **l’onglet Puces** . 
  
Pour obtenir une référence à la cellule BulletString par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :** |Para.Bullet[ *i*  ] où *i*  = <1>, 2, 3, ... |

Pour obtenir une référence à la cellule Bullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 

||Valeur |
|:-----|:-----|
|**Index de la section :** |**visSectionParagraph** |
|**Index de la ligne :**  |**visRowParagraph** +   *i* où *i* = 0, 1, 2, ... |
|**Index de la cellule :** |**visBulletIndex** |
