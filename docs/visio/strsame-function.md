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
description: Détermine si les chaînes sont identiques. Elle renvoie TRUE si elles sont identiques et FALSe si elles ne le sont pas.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428682"
---
# <a name="strsame-function"></a><span data-ttu-id="ad32f-104">Fonction STRSAME</span><span class="sxs-lookup"><span data-stu-id="ad32f-104">STRSAME Function</span></span>

<span data-ttu-id="ad32f-105">Détermine si les chaînes sont identiques.</span><span class="sxs-lookup"><span data-stu-id="ad32f-105">Determines whether strings are the same.</span></span> <span data-ttu-id="ad32f-106">Elle renvoie TRUE si elles sont identiques et FALSe si elles ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="ad32f-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ad32f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad32f-107">Syntax</span></span>

<span data-ttu-id="ad32f-108">STRSAME ("\* \* *Chaîne1* \* *", "* \* *Chaîne2* \* \*", \* \* *ignoreCase* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ad32f-108">STRSAME (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *ignoreCase* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ad32f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad32f-109">Parameters</span></span>

|<span data-ttu-id="ad32f-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ad32f-110">**Name**</span></span>|<span data-ttu-id="ad32f-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ad32f-111">**Required/Optional**</span></span>|<span data-ttu-id="ad32f-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad32f-112">**Data Type**</span></span>|<span data-ttu-id="ad32f-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="ad32f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ad32f-114">_string1_</span><span class="sxs-lookup"><span data-stu-id="ad32f-114">_string1_</span></span> <br/> |<span data-ttu-id="ad32f-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ad32f-115">Required</span></span>  <br/> |<span data-ttu-id="ad32f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="ad32f-116">**String**</span></span> <br/> |<span data-ttu-id="ad32f-117">Première chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="ad32f-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="ad32f-118">_string2_</span><span class="sxs-lookup"><span data-stu-id="ad32f-118">_string2_</span></span> <br/> |<span data-ttu-id="ad32f-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ad32f-119">Required</span></span>  <br/> |<span data-ttu-id="ad32f-120">**String**</span><span class="sxs-lookup"><span data-stu-id="ad32f-120">**String**</span></span> <br/> |<span data-ttu-id="ad32f-121">Deuxième chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="ad32f-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="ad32f-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="ad32f-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="ad32f-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ad32f-123">Optional</span></span>  <br/> |<span data-ttu-id="ad32f-124">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="ad32f-124">**Boolean**</span></span> <br/> |<span data-ttu-id="ad32f-125">Valeur TRUE pour ne pas tenir compte de la casse et valeur FALSE pour tenir compte de la casse dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ad32f-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="ad32f-126">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ad32f-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ad32f-127">Return value</span></span>

<span data-ttu-id="ad32f-128">Booléen</span><span class="sxs-lookup"><span data-stu-id="ad32f-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad32f-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad32f-129">Remarks</span></span>

<span data-ttu-id="ad32f-130">Pour comparer des chaînes multi-octets ou pour effectuer des comparaisons en utilisant les règles de casse pour un paramètre régional spécifique, utilisez la fonction STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="ad32f-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ad32f-131">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="ad32f-131">Example 1</span></span>

<span data-ttu-id="ad32f-132">STRSAME ("cat", "Dog")</span><span class="sxs-lookup"><span data-stu-id="ad32f-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="ad32f-133">Renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ad32f-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="ad32f-134">Example 2</span></span>

<span data-ttu-id="ad32f-135">STRSAME ("cat", "cat")</span><span class="sxs-lookup"><span data-stu-id="ad32f-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="ad32f-136">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ad32f-137">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="ad32f-137">Example 3</span></span>

<span data-ttu-id="ad32f-138">STRSAME("chat","chat", TRUE)</span><span class="sxs-lookup"><span data-stu-id="ad32f-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="ad32f-139">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="ad32f-140">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="ad32f-140">Example 4</span></span>

<span data-ttu-id="ad32f-141">STRSAME ("cat", "CAT")</span><span class="sxs-lookup"><span data-stu-id="ad32f-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="ad32f-142">Renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="ad32f-143">Exemple 5</span><span class="sxs-lookup"><span data-stu-id="ad32f-143">Example 5</span></span>

<span data-ttu-id="ad32f-144">STRSAME("chat","CHAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="ad32f-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="ad32f-145">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="ad32f-146">Exemple 6</span><span class="sxs-lookup"><span data-stu-id="ad32f-146">Example 6</span></span>

<span data-ttu-id="ad32f-147">STRSAME("chât","CHAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="ad32f-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="ad32f-148">Renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="ad32f-149">Exemple 7</span><span class="sxs-lookup"><span data-stu-id="ad32f-149">Example 7</span></span>

<span data-ttu-id="ad32f-150">STRSAME("chât","CHÂT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="ad32f-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="ad32f-151">Renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="ad32f-151">Returns TRUE.</span></span>
  

