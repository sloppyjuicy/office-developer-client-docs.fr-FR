---
title: FIND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426575"
---
# <a name="find-function"></a><span data-ttu-id="81883-103">Fonction FIND</span><span class="sxs-lookup"><span data-stu-id="81883-103">FIND Function</span></span>

<span data-ttu-id="81883-104">Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.</span><span class="sxs-lookup"><span data-stu-id="81883-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="81883-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81883-105">Syntax</span></span>

<span data-ttu-id="81883-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="81883-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="81883-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81883-107">Parameters</span></span>

|<span data-ttu-id="81883-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="81883-108">**Name**</span></span>|<span data-ttu-id="81883-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="81883-109">**Required/Optional**</span></span>|<span data-ttu-id="81883-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="81883-110">**Data Type**</span></span>|<span data-ttu-id="81883-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="81883-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="81883-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="81883-112">_find_text_</span></span> <br/> |<span data-ttu-id="81883-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="81883-113">Required</span></span>  <br/> |<span data-ttu-id="81883-114">**String**</span><span class="sxs-lookup"><span data-stu-id="81883-114">**String**</span></span> <br/> |<span data-ttu-id="81883-115">Chaîne de texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="81883-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="81883-116">_format_</span><span class="sxs-lookup"><span data-stu-id="81883-116">_format_</span></span> <br/> |<span data-ttu-id="81883-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="81883-117">Required</span></span>  <br/> |<span data-ttu-id="81883-118">**String**</span><span class="sxs-lookup"><span data-stu-id="81883-118">**String**</span></span> <br/> |<span data-ttu-id="81883-119">Chaîne de texte qui contient le texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="81883-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="81883-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="81883-120">_start_num_</span></span> <br/> |<span data-ttu-id="81883-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="81883-121">Optional</span></span>  <br/> |<span data-ttu-id="81883-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="81883-122">**Number**</span></span> <br/> |<span data-ttu-id="81883-123">Caractère auquel débute la recherche.</span><span class="sxs-lookup"><span data-stu-id="81883-123">The character at which to start the search.</span></span> <span data-ttu-id="81883-124">Le premier caractère de  _within_text_ est 1.</span><span class="sxs-lookup"><span data-stu-id="81883-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="81883-125">Si  _start_num_ est manquant, il est supposé être 1.</span><span class="sxs-lookup"><span data-stu-id="81883-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="81883-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="81883-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="81883-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="81883-127">Optional</span></span>  <br/> |<span data-ttu-id="81883-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="81883-128">**Boolean**</span></span> <br/> |<span data-ttu-id="81883-129">Par défaut, la fonction FIND respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="81883-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="81883-130">Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="81883-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="81883-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81883-131">Return value</span></span>

<span data-ttu-id="81883-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="81883-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81883-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="81883-133">Remarks</span></span>

<span data-ttu-id="81883-134">Si la fonction FIND détecte plusieurs correspondances, elle renvoie la position de début de la première chaîne.</span><span class="sxs-lookup"><span data-stu-id="81883-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="81883-135">_L find_text_ argument ne considère pas les caractères comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="81883-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="81883-136">Si  _find_text_:</span><span class="sxs-lookup"><span data-stu-id="81883-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="81883-137">Est vide («  »), FIND correspond au premier caractère de la chaîne de recherche (autrement dit, le caractère numéro  _start_num_ ou 1).</span><span class="sxs-lookup"><span data-stu-id="81883-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="81883-138">N’apparaît pas  _dans within_text_, FIND renvoie la #VALUE!</span><span class="sxs-lookup"><span data-stu-id="81883-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="81883-139">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="81883-139">error value.</span></span> 
    
<span data-ttu-id="81883-140">Si  _start_num_:</span><span class="sxs-lookup"><span data-stu-id="81883-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="81883-141">n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR!</span><span class="sxs-lookup"><span data-stu-id="81883-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="81883-142">;</span><span class="sxs-lookup"><span data-stu-id="81883-142">error value.</span></span> 
    
- <span data-ttu-id="81883-143">Est supérieur à la longueur de  _within_text_, FINDreturns le #VALUE!</span><span class="sxs-lookup"><span data-stu-id="81883-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="81883-144">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="81883-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="81883-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="81883-145">Example</span></span>

<span data-ttu-id="81883-146">FIND ("2003";"20 janvier 2003")</span><span class="sxs-lookup"><span data-stu-id="81883-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="81883-147">Renvoie 12.</span><span class="sxs-lookup"><span data-stu-id="81883-147">Returns 12.</span></span> 
  

