---
title: Type / C, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Définit le type du point de connexion.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415235"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="f25df-103">Type / C, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="f25df-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="f25df-104">Définit le type du point de connexion.</span><span class="sxs-lookup"><span data-stu-id="f25df-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="f25df-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f25df-105">**Value**</span></span>|<span data-ttu-id="f25df-106">**Type**</span><span class="sxs-lookup"><span data-stu-id="f25df-106">**Type**</span></span>|<span data-ttu-id="f25df-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="f25df-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f25df-108">0</span><span class="sxs-lookup"><span data-stu-id="f25df-108">0</span></span>  <br/> |<span data-ttu-id="f25df-109">Vers l’intérieur</span><span class="sxs-lookup"><span data-stu-id="f25df-109">Inward</span></span>  <br/> |<span data-ttu-id="f25df-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="f25df-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="f25df-111">1 </span><span class="sxs-lookup"><span data-stu-id="f25df-111">1</span></span>  <br/> |<span data-ttu-id="f25df-112">Vers l’extérieur</span><span class="sxs-lookup"><span data-stu-id="f25df-112">Outward</span></span>  <br/> |<span data-ttu-id="f25df-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="f25df-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="f25df-114">2 </span><span class="sxs-lookup"><span data-stu-id="f25df-114">2</span></span>  <br/> |<span data-ttu-id="f25df-115">Vers &amp; l’intérieur vers l’extérieur</span><span class="sxs-lookup"><span data-stu-id="f25df-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="f25df-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="f25df-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f25df-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="f25df-117">Remarks</span></span>

<span data-ttu-id="f25df-p101">Vous pouvez également définir le type du point de connexion en choisissant l’outil **Lien**, en sélectionnant une forme et en cliquant avec le bouton droit de la souris sur un point de connexion. Dans ce cas, vous devez utiliser le mode [développeur](run-in-developer-mode-display-the-developer-tab.md).</span><span class="sxs-lookup"><span data-stu-id="f25df-p101">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point. To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="f25df-120">Pour obtenir une référence à la cellule Type / C par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f25df-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f25df-121">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="f25df-121">Cell name:</span></span>  <br/> |<span data-ttu-id="f25df-122">Connections.Type[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f25df-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f25df-123">Pour obtenir une référence à la cellule Type / C par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f25df-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f25df-124">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f25df-124">Section index:</span></span>  <br/> |<span data-ttu-id="f25df-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="f25df-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="f25df-126">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f25df-126">Row index:</span></span>  <br/> |<span data-ttu-id="f25df-127">**visRowConnectionPts**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f25df-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f25df-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f25df-128">Cell index:</span></span>  <br/> |<span data-ttu-id="f25df-129">**visCnnctType** (lignes non étendues) **visCnnctC** (lignes étendues)</span><span class="sxs-lookup"><span data-stu-id="f25df-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="f25df-130">Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.</span><span class="sxs-lookup"><span data-stu-id="f25df-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

