---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l'orthographe est corrigée automatiquement et si les fautes d'orthographe s'affichent pour la forme sélectionnée. Prend une valeur booléenne.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357224"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="cb326-104">NoProofing Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="cb326-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="cb326-105">Détermine si l'orthographe est corrigée automatiquement et si les fautes d'orthographe s'affichent pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="cb326-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="cb326-106">Prend une valeur **booléenne** .</span><span class="sxs-lookup"><span data-stu-id="cb326-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="cb326-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="cb326-107">**Value**</span></span>|<span data-ttu-id="cb326-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="cb326-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb326-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="cb326-109">TRUE</span></span>  <br/> |<span data-ttu-id="cb326-110">L'orthographe n'est pas corrigée automatiquement et les fautes d'orthographe ne s'affichent pas pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="cb326-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="cb326-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb326-111">FALSE</span></span>  <br/> |<span data-ttu-id="cb326-112">L'orthographe est corrigée automatiquement et des fautes d'orthographe s'affichent pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="cb326-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb326-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="cb326-113">Remarks</span></span>

<span data-ttu-id="cb326-114">Pour obtenir une référence à la cellule noProofing par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="cb326-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb326-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="cb326-115">Cell name:</span></span>  <br/> |<span data-ttu-id="cb326-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="cb326-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="cb326-117">Pour obtenir une référence à la cellule noProofing à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="cb326-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb326-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="cb326-118">Section index:</span></span>  <br/> |<span data-ttu-id="cb326-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="cb326-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cb326-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="cb326-120">Row index:</span></span>  <br/> |<span data-ttu-id="cb326-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="cb326-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="cb326-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cb326-122">Cell index:</span></span>  <br/> |<span data-ttu-id="cb326-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="cb326-123">**visObjNoProofing**</span></span> <br/> |
   

