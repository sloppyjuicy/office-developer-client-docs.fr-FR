---
title: NoProofing, cellule (Section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Détermine si l’orthographe a été corrigé automatiquement, et si les fautes d’orthographe sont affichées pour la forme sélectionnée. Accepte une valeur booléenne.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19789170"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="3df96-104">NoProofing, cellule (Section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="3df96-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="3df96-105">Détermine si l’orthographe a été corrigé automatiquement, et si les fautes d’orthographe sont affichées pour la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3df96-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="3df96-106">Accepte une valeur **booléenne** .</span><span class="sxs-lookup"><span data-stu-id="3df96-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="3df96-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3df96-107">**Value**</span></span>|<span data-ttu-id="3df96-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="3df96-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3df96-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="3df96-109">TRUE</span></span>  <br/> |<span data-ttu-id="3df96-110">Orthographe n’est pas corrigé automatiquement et les fautes d’orthographe ne sont pas affichées de la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3df96-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="3df96-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="3df96-111">FALSE</span></span>  <br/> |<span data-ttu-id="3df96-112">Corrigé l’orthographe et les fautes d’orthographe sont affichés de la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3df96-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3df96-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3df96-113">Remarks</span></span>

<span data-ttu-id="3df96-114">Pour obtenir une référence à la cellule NoProofing par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="3df96-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3df96-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3df96-115">Cell name:</span></span>  <br/> |<span data-ttu-id="3df96-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="3df96-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="3df96-117">Pour obtenir une référence à la cellule NoProofing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3df96-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3df96-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3df96-118">Section index:</span></span>  <br/> |<span data-ttu-id="3df96-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3df96-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3df96-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3df96-120">Row index:</span></span>  <br/> |<span data-ttu-id="3df96-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="3df96-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="3df96-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3df96-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3df96-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="3df96-123">**visObjNoProofing**</span></span> <br/> |
   

