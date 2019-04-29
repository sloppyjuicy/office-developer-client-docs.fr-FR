---
title: PaperSource, cellule (section PrintProperties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Détermine la source de papier pour la page.
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406758"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="981be-103">PaperSource, cellule (section PrintProperties)</span><span class="sxs-lookup"><span data-stu-id="981be-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="981be-104">Détermine la source de papier pour la page.</span><span class="sxs-lookup"><span data-stu-id="981be-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="981be-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="981be-105">Remarks</span></span>

<span data-ttu-id="981be-106">Ce paramètre correspond au paramètre **Source** de la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis, sous l’onglet **Configuration**, cliquez sur le bouton **Configuration**).</span><span class="sxs-lookup"><span data-stu-id="981be-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="981be-107">Les valeurs numériques de cette cellule correspondent aux constantes (portant le préfixe DMBIN) définies pour les sélections d'emplacement dans le fichier Microsoft Windows WinGDI. h; par exemple, la valeur 7 représente DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="981be-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="981be-108">Pour obtenir une référence à la cellule PaperSource par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="981be-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="981be-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="981be-109">Cell name:</span></span>  <br/> |<span data-ttu-id="981be-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="981be-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="981be-111">Pour obtenir une référence à la cellule PaperSource à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="981be-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="981be-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="981be-112">Section index:</span></span>  <br/> |<span data-ttu-id="981be-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="981be-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="981be-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="981be-114">Row index:</span></span>  <br/> |<span data-ttu-id="981be-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="981be-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="981be-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="981be-116">Cell index:</span></span>  <br/> |<span data-ttu-id="981be-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="981be-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

