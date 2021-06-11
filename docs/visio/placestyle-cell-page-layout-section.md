---
title: PlaceStyle, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Détermine la manière dont sont placées les formes sur la page lorsque vous les disposez à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis sur Autres options de disposition).
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420800"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="f71a4-103">PlaceStyle, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="f71a4-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="f71a4-104">Détermine la manière dont sont placées les formes sur la page lorsque vous les disposez à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis sur **Autres options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="f71a4-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f71a4-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f71a4-105">Remarks</span></span>

<span data-ttu-id="f71a4-106">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Configurer la disposition**.</span><span class="sxs-lookup"><span data-stu-id="f71a4-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="f71a4-107">Pour obtenir une référence à la cellule PlaceStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f71a4-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f71a4-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f71a4-108">Cell name:</span></span>  <br/> |<span data-ttu-id="f71a4-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="f71a4-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="f71a4-110">Pour obtenir une référence à la cellule PlaceStyle à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f71a4-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f71a4-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f71a4-111">Section index:</span></span>  <br/> |<span data-ttu-id="f71a4-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f71a4-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f71a4-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f71a4-113">Row index:</span></span>  <br/> |<span data-ttu-id="f71a4-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f71a4-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="f71a4-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f71a4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="f71a4-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="f71a4-116">**visPLOPlaceStyle**</span></span> <br/> |
   

