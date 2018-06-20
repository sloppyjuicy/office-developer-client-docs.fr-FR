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
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789954"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="038d1-103">Type / C, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="038d1-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="038d1-104">Définit le type du point de connexion.</span><span class="sxs-lookup"><span data-stu-id="038d1-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="038d1-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="038d1-105">**Value**</span></span>|<span data-ttu-id="038d1-106">**Type**</span><span class="sxs-lookup"><span data-stu-id="038d1-106">**Type**</span></span>|<span data-ttu-id="038d1-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="038d1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="038d1-108">0</span><span class="sxs-lookup"><span data-stu-id="038d1-108">0</span></span>  <br/> |<span data-ttu-id="038d1-109">Vers l'intérieur</span><span class="sxs-lookup"><span data-stu-id="038d1-109">Inward</span></span>  <br/> |<span data-ttu-id="038d1-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="038d1-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="038d1-111">1</span><span class="sxs-lookup"><span data-stu-id="038d1-111">1</span></span>  <br/> |<span data-ttu-id="038d1-112">Vers l'extérieur</span><span class="sxs-lookup"><span data-stu-id="038d1-112">Outward</span></span>  <br/> |<span data-ttu-id="038d1-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="038d1-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="038d1-114">2</span><span class="sxs-lookup"><span data-stu-id="038d1-114">2</span></span>  <br/> |<span data-ttu-id="038d1-115">Vers l’intérieur &amp; vers l’extérieur</span><span class="sxs-lookup"><span data-stu-id="038d1-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="038d1-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="038d1-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="038d1-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="038d1-117">Remarks</span></span>

<span data-ttu-id="038d1-118">Vous pouvez également définir le type de point de connexion en choisissant l’outil **connecteur** , sélectionner une forme, puis cliquez sur un point de connexion.</span><span class="sxs-lookup"><span data-stu-id="038d1-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="038d1-119">Pour ce faire, vous devez exécuter en mode [développeur](run-in-developer-mode-display-the-developer-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="038d1-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="038d1-120">Pour obtenir une référence au Type / C, cellule par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="038d1-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="038d1-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="038d1-121">Cell name:</span></span>  <br/> |<span data-ttu-id="038d1-122">Connections.Type [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="038d1-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="038d1-123">Pour obtenir une référence au Type / C, cellule par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="038d1-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="038d1-124">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="038d1-124">Section index:</span></span>  <br/> |<span data-ttu-id="038d1-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="038d1-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="038d1-126">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="038d1-126">Row index:</span></span>  <br/> |<span data-ttu-id="038d1-127">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="038d1-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="038d1-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="038d1-128">Cell index:</span></span>  <br/> |<span data-ttu-id="038d1-129">**visCnnctType** (lignes non étendues) **visCnnctC** (lignes étendues)</span><span class="sxs-lookup"><span data-stu-id="038d1-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="038d1-130">Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.</span><span class="sxs-lookup"><span data-stu-id="038d1-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

