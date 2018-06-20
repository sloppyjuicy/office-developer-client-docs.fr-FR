---
title: SubAddress, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Indique un emplacement au sein du document cible vers lequel établir un lien.
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789841"
---
# <a name="subaddress-cell-hyperlinks-section"></a>SubAddress, cellule (section Hyperlinks)

Indique un emplacement au sein du document cible vers lequel établir un lien.
  
## <a name="remarks"></a>Remarques

Par exemple, si la cellule Address est « Drawing1.vsdx », la cellule SubAddress peut spécifier un nom de page tel que « Page 3 ». Si la cellule Address est le fichier Microsoft Excel « Samples.xlsx », la valeur de cette cellule peut être une feuille de calcul ou une plage dans une feuille de calcul, tel que « Fonctions de feuille de calcul » ou « Sheet1 ! A1 : D10 ». Si la cellule Address est «http://www.microsoft.com/office/», la valeur de cette cellule peut être un point d’ancrage nommé dans le document, tel que « solutions ».
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **liens hypertexte** (dans le groupe **liens** sous l’onglet **Insertion** , cliquez sur **lien hypertexte**).
  
Pour obtenir une référence à la cellule SubAddress par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *nom* . SubAddress où le lien hypertexte *.name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule **SubAddress** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkSubAddress** <br/> |
   

