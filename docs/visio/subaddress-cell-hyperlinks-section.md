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
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349321"
---
# <a name="subaddress-cell-hyperlinks-section"></a>SubAddress, cellule (section Hyperlinks)

Indique un emplacement au sein du document cible vers lequel établir un lien.
  
## <a name="remarks"></a>Remarques

Par exemple, si la cellule Address est « Drawing1.vsdx », la cellule SubAddress peut spécifier un nom de page tel que « Page-3 ». Si la cellule Address est le fichier Microsoft Excel « Samples.xlsx », la valeur de cette cellule peut être une feuille de calcul ou une plage dans une feuille de calcul, telle que « Fonctions de feuille de calcul » ou « Feuille1 ! A1:D10 ». Si la cellule Address est « », la valeur de cette cellule peut être une ancre nommée dans le document, telle que https://www.microsoft.com/office/ « solutions ».
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Liens hypertexte** (dans le groupe **Liens** sous l’onglet **Insertion**, cliquez sur **Lien hypertexte**).
  
Pour obtenir une référence à la cellule SubAddress à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Lien hypertexte.  *nom*  . Sous-adresse où Hyperlink  *.name*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la **cellule SubAddress** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkSubAddress** <br/> |
   

