---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l’orthographe est corrigée automatiquement et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Prend une valeur boolé américaine.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431252"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="fd4f4-104">NoProofing Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="fd4f4-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fd4f4-105">Détermine si l’orthographe est corrigée automatiquement et si les fautes d’orthographe sont affichées pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="fd4f4-106">Prend une **valeur boolé** américaine.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="fd4f4-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="fd4f4-107">**Value**</span></span>|<span data-ttu-id="fd4f4-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd4f4-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd4f4-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="fd4f4-109">TRUE</span></span>  <br/> |<span data-ttu-id="fd4f4-110">L’orthographe n’est pas corrigée automatiquement et les fautes d’orthographe ne sont pas affichées pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="fd4f4-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd4f4-111">FALSE</span></span>  <br/> |<span data-ttu-id="fd4f4-112">L’orthographe est automatiquement corrigée et les fautes d’orthographe sont affichées pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd4f4-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd4f4-113">Remarks</span></span>

<span data-ttu-id="fd4f4-114">Pour obtenir une référence à la cellule NoProofing par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="fd4f4-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd4f4-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="fd4f4-115">Cell name:</span></span>  <br/> |<span data-ttu-id="fd4f4-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="fd4f4-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="fd4f4-117">Pour obtenir une référence à la cellule NoProofing à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fd4f4-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd4f4-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fd4f4-118">Section index:</span></span>  <br/> |<span data-ttu-id="fd4f4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd4f4-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fd4f4-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fd4f4-120">Row index:</span></span>  <br/> |<span data-ttu-id="fd4f4-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="fd4f4-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="fd4f4-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fd4f4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fd4f4-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="fd4f4-123">**visObjNoProofing**</span></span> <br/> |
   

