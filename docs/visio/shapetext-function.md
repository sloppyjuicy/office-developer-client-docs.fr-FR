---
title: SHAPETEXT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtient le texte d'une forme.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419344"
---
# <a name="shapetext-function"></a><span data-ttu-id="b9651-103">Fonction SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="b9651-103">SHAPETEXT Function</span></span>

<span data-ttu-id="b9651-104">Obtient le texte d'une forme.</span><span class="sxs-lookup"><span data-stu-id="b9651-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b9651-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9651-105">Syntax</span></span>

<span data-ttu-id="b9651-106">SHAPETEXT (\* \* *ShapeName! TheText* \* \* \* \* *[, indicateur]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b9651-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b9651-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9651-107">Parameters</span></span>

|<span data-ttu-id="b9651-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b9651-108">**Name**</span></span>|<span data-ttu-id="b9651-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b9651-109">**Required/Optional**</span></span>|<span data-ttu-id="b9651-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b9651-110">**Data Type**</span></span>|<span data-ttu-id="b9651-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9651-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b9651-112">_ShapeName! TheText_</span><span class="sxs-lookup"><span data-stu-id="b9651-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="b9651-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b9651-113">Required</span></span>  <br/> ||<span data-ttu-id="b9651-114">Référence à la cellule nommée TheText dans la forme cible.</span><span class="sxs-lookup"><span data-stu-id="b9651-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="b9651-115">_ShapeName!_</span><span class="sxs-lookup"><span data-stu-id="b9651-115">_Shapename!_</span></span> <span data-ttu-id="b9651-116">est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="b9651-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="b9651-117">_indicateur_</span><span class="sxs-lookup"><span data-stu-id="b9651-117">_flag_</span></span> <br/> |<span data-ttu-id="b9651-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b9651-118">Optional</span></span>  <br/> |<span data-ttu-id="b9651-119">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="b9651-119">**Numeric**</span></span> <br/> |<span data-ttu-id="b9651-120">Bit qui spécifie le format du texte.</span><span class="sxs-lookup"><span data-stu-id="b9651-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="b9651-121">L’indicateur par défaut (0) présente le texte exactement tel qu’il apparaît dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b9651-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b9651-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9651-122">Return value</span></span>

<span data-ttu-id="b9651-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b9651-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9651-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9651-124">Remarks</span></span>

<span data-ttu-id="b9651-125">Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction SHAPETEXT.</span><span class="sxs-lookup"><span data-stu-id="b9651-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="b9651-126">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="b9651-126">**Flag**</span></span>|<span data-ttu-id="b9651-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9651-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9651-128">0</span><span class="sxs-lookup"><span data-stu-id="b9651-128">0</span></span>  <br/> |<span data-ttu-id="b9651-129">Présente le texte tel qu’il est affiché dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b9651-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="b9651-130">0,1</span><span class="sxs-lookup"><span data-stu-id="b9651-130">1</span></span>  <br/> |<span data-ttu-id="b9651-131">Comprend des tirets.</span><span class="sxs-lookup"><span data-stu-id="b9651-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="b9651-132">n°2</span><span class="sxs-lookup"><span data-stu-id="b9651-132">2</span></span>  <br/> |<span data-ttu-id="b9651-133">Ne comprend pas de texte développé dans les champs.</span><span class="sxs-lookup"><span data-stu-id="b9651-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="b9651-134">4</span><span class="sxs-lookup"><span data-stu-id="b9651-134">4</span></span>  <br/> |<span data-ttu-id="b9651-135">Convertit les tabulations en un espace simple.</span><span class="sxs-lookup"><span data-stu-id="b9651-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="b9651-136">8bits</span><span class="sxs-lookup"><span data-stu-id="b9651-136">8</span></span>  <br/> |<span data-ttu-id="b9651-137">Convertit les tabulations en un jeu d’espaces.</span><span class="sxs-lookup"><span data-stu-id="b9651-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="b9651-138">16 </span><span class="sxs-lookup"><span data-stu-id="b9651-138">16</span></span>  <br/> |<span data-ttu-id="b9651-139">Convertit les retours chariot et les sauts de ligne en espaces.</span><span class="sxs-lookup"><span data-stu-id="b9651-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="b9651-140">32</span><span class="sxs-lookup"><span data-stu-id="b9651-140">32</span></span>  <br/> |<span data-ttu-id="b9651-141">Convertit les guillemets typographiques en guillemets droits.</span><span class="sxs-lookup"><span data-stu-id="b9651-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="b9651-142">64</span><span class="sxs-lookup"><span data-stu-id="b9651-142">64</span></span>  <br/> |<span data-ttu-id="b9651-143">Convertit plusieurs espaces adjacents en un seul espace.</span><span class="sxs-lookup"><span data-stu-id="b9651-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="b9651-144">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b9651-144">Example 1</span></span>

<span data-ttu-id="b9651-145">SHAPETEXT (Sheetn! theText)</span><span class="sxs-lookup"><span data-stu-id="b9651-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="b9651-146">Renvoie le texte de la forme nommée feuilleN, exactement tel qu’il apparaît dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b9651-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b9651-147">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b9651-147">Example 2</span></span>

<span data-ttu-id="b9651-148">SHAPETEXT (theText)</span><span class="sxs-lookup"><span data-stu-id="b9651-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="b9651-149">Renvoie le texte de la forme actuelle exactement tel qu’il apparaît dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b9651-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b9651-150">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b9651-150">Example 3</span></span>

<span data-ttu-id="b9651-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="b9651-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="b9651-p103">Renvoie le texte de la forme actuelle. Cet exemple convertit également les espaces adjacents en un seul espace (64), les retours chariot et les sauts de ligne en espaces (16) et les tabulations en un espace simple (4). La somme de ces indicateurs est 84.</span><span class="sxs-lookup"><span data-stu-id="b9651-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

