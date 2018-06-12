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
description: Obtient le texte d’une forme.
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789685"
---
# <a name="shapetext-function"></a><span data-ttu-id="b52f9-103">SHAPETEXT, fonction</span><span class="sxs-lookup"><span data-stu-id="b52f9-103">SHAPETEXT Function</span></span>

<span data-ttu-id="b52f9-104">Obtient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="b52f9-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b52f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b52f9-105">Syntax</span></span>

<span data-ttu-id="b52f9-106">SHAPETEXT (** shapename *! TheText* ** ** *[, indicateur]* **)</span><span class="sxs-lookup"><span data-stu-id="b52f9-106">SHAPETEXT (** *shapename!TheText* ** ** *[,flag]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b52f9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b52f9-107">Parameters</span></span>

|<span data-ttu-id="b52f9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b52f9-108">**Name**</span></span>|<span data-ttu-id="b52f9-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b52f9-109">**Required/Optional**</span></span>|<span data-ttu-id="b52f9-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b52f9-110">**Data Type**</span></span>|<span data-ttu-id="b52f9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b52f9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b52f9-112">_argument shapename ! TheText_</span><span class="sxs-lookup"><span data-stu-id="b52f9-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="b52f9-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b52f9-113">Required</span></span>  <br/> ||<span data-ttu-id="b52f9-114">Une référence à la cellule nommée TheText dans la forme cible.</span><span class="sxs-lookup"><span data-stu-id="b52f9-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="b52f9-115">_Argument shapename !_</span><span class="sxs-lookup"><span data-stu-id="b52f9-115">_Shapename!_</span></span> <span data-ttu-id="b52f9-116">est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="b52f9-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="b52f9-117">_indicateur_</span><span class="sxs-lookup"><span data-stu-id="b52f9-117">_flag_</span></span> <br/> |<span data-ttu-id="b52f9-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b52f9-118">Optional</span></span>  <br/> |<span data-ttu-id="b52f9-119">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="b52f9-119">**Numeric**</span></span> <br/> |<span data-ttu-id="b52f9-p102">Bit qui spécifie le format du texte. L’indicateur par défaut (0) présente le texte exactement tel qu’il apparaît dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b52f9-p102">A bit that specifies the format of the text. The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b52f9-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b52f9-122">Return value</span></span>

<span data-ttu-id="b52f9-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b52f9-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b52f9-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="b52f9-124">Remarks</span></span>

<span data-ttu-id="b52f9-125">Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction SHAPETEXT.</span><span class="sxs-lookup"><span data-stu-id="b52f9-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="b52f9-126">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="b52f9-126">**Flag**</span></span>|<span data-ttu-id="b52f9-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="b52f9-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b52f9-128">0</span><span class="sxs-lookup"><span data-stu-id="b52f9-128">0</span></span>  <br/> |<span data-ttu-id="b52f9-129">Présente le texte tel qu’il est affiché dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b52f9-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="b52f9-130">1</span><span class="sxs-lookup"><span data-stu-id="b52f9-130">1</span></span>  <br/> |<span data-ttu-id="b52f9-131">Comprend des tirets.</span><span class="sxs-lookup"><span data-stu-id="b52f9-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="b52f9-132">2</span><span class="sxs-lookup"><span data-stu-id="b52f9-132">2</span></span>  <br/> |<span data-ttu-id="b52f9-133">Ne comprend pas de texte développé dans les champs.</span><span class="sxs-lookup"><span data-stu-id="b52f9-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="b52f9-134">4</span><span class="sxs-lookup"><span data-stu-id="b52f9-134">4</span></span>  <br/> |<span data-ttu-id="b52f9-135">Convertit les tabulations en un espace simple.</span><span class="sxs-lookup"><span data-stu-id="b52f9-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="b52f9-136">8</span><span class="sxs-lookup"><span data-stu-id="b52f9-136">8</span></span>  <br/> |<span data-ttu-id="b52f9-137">Convertit les tabulations en un jeu d’espaces.</span><span class="sxs-lookup"><span data-stu-id="b52f9-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="b52f9-138">16</span><span class="sxs-lookup"><span data-stu-id="b52f9-138">16</span></span>  <br/> |<span data-ttu-id="b52f9-139">Convertit les retours chariot et les sauts de ligne en espaces.</span><span class="sxs-lookup"><span data-stu-id="b52f9-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="b52f9-140">32</span><span class="sxs-lookup"><span data-stu-id="b52f9-140">32</span></span>  <br/> |<span data-ttu-id="b52f9-141">Convertit les guillemets typographiques en guillemets droits.</span><span class="sxs-lookup"><span data-stu-id="b52f9-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="b52f9-142">64</span><span class="sxs-lookup"><span data-stu-id="b52f9-142">64</span></span>  <br/> |<span data-ttu-id="b52f9-143">Convertit plusieurs espaces adjacents en un seul espace.</span><span class="sxs-lookup"><span data-stu-id="b52f9-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="b52f9-144">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b52f9-144">Example 1</span></span>

<span data-ttu-id="b52f9-145">SHAPETEXT(sheetN!TheText)</span><span class="sxs-lookup"><span data-stu-id="b52f9-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="b52f9-146">Renvoie le texte de la forme nommée feuilleN, exactement tel qu’il apparaît dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b52f9-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b52f9-147">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b52f9-147">Example 2</span></span>

<span data-ttu-id="b52f9-148">SHAPETEXT(TheText)</span><span class="sxs-lookup"><span data-stu-id="b52f9-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="b52f9-149">Renvoie le texte de la forme actuelle exactement tel qu’il apparaît dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b52f9-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b52f9-150">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b52f9-150">Example 3</span></span>

<span data-ttu-id="b52f9-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="b52f9-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="b52f9-p103">Renvoie le texte de la forme actuelle. Cet exemple convertit également les espaces adjacents en un seul espace (64), les retours chariot et les sauts de ligne en espaces (16) et les tabulations en un espace simple (4). La somme de ces indicateurs est 84.</span><span class="sxs-lookup"><span data-stu-id="b52f9-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

