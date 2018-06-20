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
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789216"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="9aef2-103">PaperSource, cellule (section PrintProperties)</span><span class="sxs-lookup"><span data-stu-id="9aef2-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="9aef2-104">Détermine la source de papier pour la page.</span><span class="sxs-lookup"><span data-stu-id="9aef2-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9aef2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="9aef2-105">Remarks</span></span>

<span data-ttu-id="9aef2-106">Ce paramètre correspond au paramètre **d’Alimentation papier** dans la boîte de dialogue **Configuration de l’impression** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** et cliquez sur l’onglet **Configuration de l’impression** , **le programme d’installation**).</span><span class="sxs-lookup"><span data-stu-id="9aef2-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="9aef2-107">Les valeurs numériques de cette cellule correspondent à des constantes (ayant pour préfixe DMBIN) définies pour les sélections de Corbeille dans le fichier wingdi.h de Microsoft Windows ; par exemple, la valeur 7 représente DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="9aef2-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="9aef2-108">Pour obtenir une référence à la cellule PaperSource par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="9aef2-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9aef2-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9aef2-109">Cell name:</span></span>  <br/> |<span data-ttu-id="9aef2-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="9aef2-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="9aef2-111">Pour obtenir une référence à la cellule PaperSource par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9aef2-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9aef2-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9aef2-112">Section index:</span></span>  <br/> |<span data-ttu-id="9aef2-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9aef2-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9aef2-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9aef2-114">Row index:</span></span>  <br/> |<span data-ttu-id="9aef2-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="9aef2-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="9aef2-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9aef2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9aef2-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="9aef2-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

