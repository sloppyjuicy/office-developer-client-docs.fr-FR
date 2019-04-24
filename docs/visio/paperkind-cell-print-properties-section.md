---
title: PaperKind, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Indique le type de papier sur lequel imprimer la page.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327061"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="7feb4-103">PaperKind, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="7feb4-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="7feb4-104">Indique le type de papier sur lequel imprimer la page.</span><span class="sxs-lookup"><span data-stu-id="7feb4-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7feb4-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="7feb4-105">Remarks</span></span>

<span data-ttu-id="7feb4-106">Ce paramètre correspond au paramètre **taille du papier** de la boîte de dialogue Configuration de l' **impression** (sous l'onglet **création** , cliquez sur la flèche **mise en page** , puis, sous l'onglet **configuration** , cliquez sur le bouton **configuration** ).</span><span class="sxs-lookup"><span data-stu-id="7feb4-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="7feb4-107">Les valeurs numériques de cette cellule correspondent aux constantes (portant le préfixe DMPAPER) définies pour les sélections de papier dans le fichier Microsoft Windows WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="7feb4-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="7feb4-108">Pour obtenir une référence à la cellule PaperKind par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7feb4-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7feb4-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7feb4-109">Cell name:</span></span>  <br/> |<span data-ttu-id="7feb4-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="7feb4-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="7feb4-111">Pour obtenir une référence à la cellule PaperKind à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7feb4-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7feb4-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7feb4-112">Section index:</span></span>  <br/> |<span data-ttu-id="7feb4-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="7feb4-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7feb4-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7feb4-114">Row index:</span></span>  <br/> |<span data-ttu-id="7feb4-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="7feb4-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="7feb4-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7feb4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7feb4-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="7feb4-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

