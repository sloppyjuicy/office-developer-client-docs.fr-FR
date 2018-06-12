---
title: STRSAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Détermine si les chaînes sont identiques. Elle renvoie la valeur TRUE si elles sont identiques et FALSE si elles ne sont pas.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789813"
---
# <a name="strsame-function"></a><span data-ttu-id="fb464-104">STRSAME, fonction</span><span class="sxs-lookup"><span data-stu-id="fb464-104">STRSAME Function</span></span>

<span data-ttu-id="fb464-105">Détermine si les chaînes sont identiques.</span><span class="sxs-lookup"><span data-stu-id="fb464-105">Determines whether strings are the same.</span></span> <span data-ttu-id="fb464-106">Elle renvoie la valeur TRUE si elles sont identiques et FALSE si elles ne sont pas.</span><span class="sxs-lookup"><span data-stu-id="fb464-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fb464-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb464-107">Syntax</span></span>

<span data-ttu-id="fb464-108">STRSAME (« ** *chaîne1* ** «, » ** *chaîne2* ** », ** *ignoreCase* **)</span><span class="sxs-lookup"><span data-stu-id="fb464-108">STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fb464-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb464-109">Parameters</span></span>

|<span data-ttu-id="fb464-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="fb464-110">**Name**</span></span>|<span data-ttu-id="fb464-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="fb464-111">**Required/Optional**</span></span>|<span data-ttu-id="fb464-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="fb464-112">**Data Type**</span></span>|<span data-ttu-id="fb464-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="fb464-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fb464-114">_chaîne string1_</span><span class="sxs-lookup"><span data-stu-id="fb464-114">_string1_</span></span> <br/> |<span data-ttu-id="fb464-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fb464-115">Required</span></span>  <br/> |<span data-ttu-id="fb464-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb464-116">**String**</span></span> <br/> |<span data-ttu-id="fb464-117">Première chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="fb464-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="fb464-118">_chaîne2_</span><span class="sxs-lookup"><span data-stu-id="fb464-118">_string2_</span></span> <br/> |<span data-ttu-id="fb464-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fb464-119">Required</span></span>  <br/> |<span data-ttu-id="fb464-120">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb464-120">**String**</span></span> <br/> |<span data-ttu-id="fb464-121">Deuxième chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="fb464-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="fb464-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="fb464-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="fb464-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="fb464-123">Optional</span></span>  <br/> |<span data-ttu-id="fb464-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fb464-124">**Boolean**</span></span> <br/> |<span data-ttu-id="fb464-p103">Valeur TRUE pour ne pas tenir compte de la casse et valeur FALSE pour tenir compte de la casse dans la comparaison. La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="fb464-p103">TRUE to ignore the case and FALSE to compare the case. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fb464-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="fb464-127">Return value</span></span>

<span data-ttu-id="fb464-128">Booléenne</span><span class="sxs-lookup"><span data-stu-id="fb464-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb464-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb464-129">Remarks</span></span>

<span data-ttu-id="fb464-130">Pour comparer des chaînes multi-octets ou pour effectuer des comparaisons en utilisant les règles de casse pour un paramètre régional spécifique, utilisez la fonction STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="fb464-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="fb464-131">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="fb464-131">Example 1</span></span>

<span data-ttu-id="fb464-132">STRSAME("chat","chien")</span><span class="sxs-lookup"><span data-stu-id="fb464-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="fb464-133">Renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="fb464-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fb464-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="fb464-134">Example 2</span></span>

<span data-ttu-id="fb464-135">STRSAME("chat","chat")</span><span class="sxs-lookup"><span data-stu-id="fb464-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="fb464-136">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="fb464-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fb464-137">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="fb464-137">Example 3</span></span>

<span data-ttu-id="fb464-138">STRSAME("chat","chat", TRUE)</span><span class="sxs-lookup"><span data-stu-id="fb464-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="fb464-139">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="fb464-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="fb464-140">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="fb464-140">Example 4</span></span>

<span data-ttu-id="fb464-141">STRSAME("chat","CHAT")</span><span class="sxs-lookup"><span data-stu-id="fb464-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="fb464-142">Renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="fb464-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="fb464-143">Exemple 5</span><span class="sxs-lookup"><span data-stu-id="fb464-143">Example 5</span></span>

<span data-ttu-id="fb464-144">STRSAME("chat","CHAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="fb464-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="fb464-145">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="fb464-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="fb464-146">Exemple 6</span><span class="sxs-lookup"><span data-stu-id="fb464-146">Example 6</span></span>

<span data-ttu-id="fb464-147">STRSAME("chât","CHAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="fb464-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="fb464-148">Renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="fb464-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="fb464-149">Exemple 7</span><span class="sxs-lookup"><span data-stu-id="fb464-149">Example 7</span></span>

<span data-ttu-id="fb464-150">STRSAME("chât","CHÂT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="fb464-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="fb464-151">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="fb464-151">Returns TRUE.</span></span>
  

