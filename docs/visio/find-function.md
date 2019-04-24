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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322497"
---
# <a name="find-function"></a><span data-ttu-id="cc3b0-103">Fonction FIND</span><span class="sxs-lookup"><span data-stu-id="cc3b0-103">FIND Function</span></span>

<span data-ttu-id="cc3b0-104">Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cc3b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc3b0-105">Syntax</span></span>

<span data-ttu-id="cc3b0-106">Find (\* \* *texte_cherché* \* \*, \* \* *dans_texte* \* *, [* \* *no_départ* \* *], [* \* *ignore_case* \* \*])</span><span class="sxs-lookup"><span data-stu-id="cc3b0-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cc3b0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc3b0-107">Parameters</span></span>

|<span data-ttu-id="cc3b0-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-108">**Name**</span></span>|<span data-ttu-id="cc3b0-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-109">**Required/Optional**</span></span>|<span data-ttu-id="cc3b0-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-110">**Data Type**</span></span>|<span data-ttu-id="cc3b0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cc3b0-112">_accepte_</span><span class="sxs-lookup"><span data-stu-id="cc3b0-112">_find_text_</span></span> <br/> |<span data-ttu-id="cc3b0-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cc3b0-113">Required</span></span>  <br/> |<span data-ttu-id="cc3b0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-114">**String**</span></span> <br/> |<span data-ttu-id="cc3b0-115">Chaîne de texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="cc3b0-116">_format_</span><span class="sxs-lookup"><span data-stu-id="cc3b0-116">_format_</span></span> <br/> |<span data-ttu-id="cc3b0-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cc3b0-117">Required</span></span>  <br/> |<span data-ttu-id="cc3b0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-118">**String**</span></span> <br/> |<span data-ttu-id="cc3b0-119">Chaîne de texte qui contient le texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="cc3b0-120">_no_départ_</span><span class="sxs-lookup"><span data-stu-id="cc3b0-120">_start_num_</span></span> <br/> |<span data-ttu-id="cc3b0-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="cc3b0-121">Optional</span></span>  <br/> |<span data-ttu-id="cc3b0-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-122">**Number**</span></span> <br/> |<span data-ttu-id="cc3b0-123">Caractère auquel débute la recherche.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-123">The character at which to start the search.</span></span> <span data-ttu-id="cc3b0-124">Le premier caractère dans _dans_texte_ est 1.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="cc3b0-125">Si _no_départ_ est manquant, il est supposé égal à 1.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="cc3b0-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="cc3b0-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="cc3b0-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="cc3b0-127">Optional</span></span>  <br/> |<span data-ttu-id="cc3b0-128">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="cc3b0-128">**Boolean**</span></span> <br/> |<span data-ttu-id="cc3b0-129">Par défaut, la fonction FIND respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="cc3b0-130">Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cc3b0-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc3b0-131">Return value</span></span>

<span data-ttu-id="cc3b0-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc3b0-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc3b0-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc3b0-133">Remarks</span></span>

<span data-ttu-id="cc3b0-134">Si la fonction FIND détecte plusieurs correspondances, elle renvoie la position de début de la première chaîne.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="cc3b0-135">L'argument _texte_cherché_ ne tient pas compte des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="cc3b0-136">Si _texte_cherché_:</span><span class="sxs-lookup"><span data-stu-id="cc3b0-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="cc3b0-137">Est vide (""), FIND correspond au premier caractère de la chaîne de recherche (c'est-à-dire, le caractère numéroté _no_départ_ ou 1).</span><span class="sxs-lookup"><span data-stu-id="cc3b0-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="cc3b0-138">N'apparaît pas dans _dans_texte_, Find renvoie la #VALUE!</span><span class="sxs-lookup"><span data-stu-id="cc3b0-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="cc3b0-139">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-139">error value.</span></span> 
    
<span data-ttu-id="cc3b0-140">Si _no_départ_:</span><span class="sxs-lookup"><span data-stu-id="cc3b0-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="cc3b0-141">n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR!</span><span class="sxs-lookup"><span data-stu-id="cc3b0-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="cc3b0-142">;</span><span class="sxs-lookup"><span data-stu-id="cc3b0-142">error value.</span></span> 
    
- <span data-ttu-id="cc3b0-143">Est supérieur à la longueur de _dans_texte_, FINDreturns le #VALUE!</span><span class="sxs-lookup"><span data-stu-id="cc3b0-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="cc3b0-144">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="cc3b0-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="cc3b0-145">Example</span></span>

<span data-ttu-id="cc3b0-146">FIND ("2003";"20 janvier 2003")</span><span class="sxs-lookup"><span data-stu-id="cc3b0-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="cc3b0-147">Renvoie 12.</span><span class="sxs-lookup"><span data-stu-id="cc3b0-147">Returns 12.</span></span> 
  

