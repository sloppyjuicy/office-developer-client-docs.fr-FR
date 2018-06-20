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
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789220"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="418bb-103">PaperKind, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="418bb-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="418bb-104">Indique le type de papier sur lequel imprimer la page.</span><span class="sxs-lookup"><span data-stu-id="418bb-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="418bb-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="418bb-105">Remarks</span></span>

<span data-ttu-id="418bb-106">Ce paramètre correspond au paramètre de **Taille de papier** dans la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis, sous l’onglet **Configuration de l’impression** , cliquez sur le bouton de **l’installation** ).</span><span class="sxs-lookup"><span data-stu-id="418bb-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="418bb-107">Les valeurs numériques de cette cellule correspondent à des constantes (ayant pour préfixe DMPAPER) définies pour les sélections de papier dans le fichier wingdi.h de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="418bb-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="418bb-108">Pour obtenir une référence à la cellule PaperKind par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="418bb-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="418bb-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="418bb-109">Cell name:</span></span>  <br/> |<span data-ttu-id="418bb-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="418bb-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="418bb-111">Pour obtenir une référence à la cellule PaperKind par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="418bb-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="418bb-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="418bb-112">Section index:</span></span>  <br/> |<span data-ttu-id="418bb-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="418bb-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="418bb-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="418bb-114">Row index:</span></span>  <br/> |<span data-ttu-id="418bb-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="418bb-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="418bb-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="418bb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="418bb-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="418bb-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

