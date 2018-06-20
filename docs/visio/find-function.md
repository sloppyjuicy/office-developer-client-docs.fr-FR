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
description: Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte recherché par rapport à sa position dans la chaîne de texte qui le contient.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788659"
---
# <a name="find-function"></a><span data-ttu-id="5da60-103">FIND, fonction</span><span class="sxs-lookup"><span data-stu-id="5da60-103">FIND Function</span></span>

<span data-ttu-id="5da60-104">Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte recherché par rapport à sa position dans la chaîne de texte qui le contient.</span><span class="sxs-lookup"><span data-stu-id="5da60-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5da60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5da60-105">Syntax</span></span>

<span data-ttu-id="5da60-106">Rechercher (** *rechercher_texte* **, ** *within_text* **, [** *start_num* **], [** *ignorer_casse* **])</span><span class="sxs-lookup"><span data-stu-id="5da60-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5da60-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5da60-107">Parameters</span></span>

|<span data-ttu-id="5da60-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5da60-108">**Name**</span></span>|<span data-ttu-id="5da60-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="5da60-109">**Required/Optional**</span></span>|<span data-ttu-id="5da60-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="5da60-110">**Data Type**</span></span>|<span data-ttu-id="5da60-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="5da60-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5da60-112">_rechercher_texte_</span><span class="sxs-lookup"><span data-stu-id="5da60-112">_find_text_</span></span> <br/> |<span data-ttu-id="5da60-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5da60-113">Required</span></span>  <br/> |<span data-ttu-id="5da60-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="5da60-114">**String**</span></span> <br/> |<span data-ttu-id="5da60-115">Chaîne de texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="5da60-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="5da60-116">_format_</span><span class="sxs-lookup"><span data-stu-id="5da60-116">_format_</span></span> <br/> |<span data-ttu-id="5da60-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5da60-117">Required</span></span>  <br/> |<span data-ttu-id="5da60-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="5da60-118">**String**</span></span> <br/> |<span data-ttu-id="5da60-119">Chaîne de texte qui contient le texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="5da60-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="5da60-120">_Start_num_</span><span class="sxs-lookup"><span data-stu-id="5da60-120">_start_num_</span></span> <br/> |<span data-ttu-id="5da60-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="5da60-121">Optional</span></span>  <br/> |<span data-ttu-id="5da60-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="5da60-122">**Number**</span></span> <br/> |<span data-ttu-id="5da60-123">Le caractère à partir duquel commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="5da60-123">The character at which to start the search.</span></span> <span data-ttu-id="5da60-124">Le premier caractère de _dans_texte_ est 1.</span><span class="sxs-lookup"><span data-stu-id="5da60-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="5da60-125">Si _start_num_ est manquant, il est supposé pour être 1.</span><span class="sxs-lookup"><span data-stu-id="5da60-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="5da60-126">_ignorer_casse_</span><span class="sxs-lookup"><span data-stu-id="5da60-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="5da60-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="5da60-127">Optional</span></span>  <br/> |<span data-ttu-id="5da60-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5da60-128">**Boolean**</span></span> <br/> |<span data-ttu-id="5da60-p102">Par défaut, la fonction FIND respecte la casse. Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="5da60-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5da60-131">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5da60-131">Return value</span></span>

<span data-ttu-id="5da60-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="5da60-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5da60-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="5da60-133">Remarks</span></span>

<span data-ttu-id="5da60-134">Si plusieurs correspondances sont trouvées, la fonction FIND renvoie la position de départ de la première correspondance dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5da60-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="5da60-135">L’argument _rechercher_texte_ ne considère aucun caractère comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="5da60-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="5da60-136">Si _find_text_:</span><span class="sxs-lookup"><span data-stu-id="5da60-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="5da60-137">Est vide (« »), FIND renvoie le premier caractère de la chaîne recherchée (c'est-à-dire, le caractère numéroté _num_départ_ ou 1).</span><span class="sxs-lookup"><span data-stu-id="5da60-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="5da60-138">N’apparaît pas dans _dans_texte_, FIND renvoie la #VALUE !</span><span class="sxs-lookup"><span data-stu-id="5da60-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="5da60-139">valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5da60-139">error value.</span></span> 
    
<span data-ttu-id="5da60-140">Si _start_num_:</span><span class="sxs-lookup"><span data-stu-id="5da60-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="5da60-p105">n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR! ;</span><span class="sxs-lookup"><span data-stu-id="5da60-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="5da60-143">Est supérieur à la longueur de _dans_texte_, Find renvoie la #VALUE !</span><span class="sxs-lookup"><span data-stu-id="5da60-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="5da60-144">valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5da60-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="5da60-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="5da60-145">Example</span></span>

<span data-ttu-id="5da60-146">FIND ("2003";"20 janvier 2003")</span><span class="sxs-lookup"><span data-stu-id="5da60-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="5da60-147">Renvoie 12.</span><span class="sxs-lookup"><span data-stu-id="5da60-147">Returns 12.</span></span> 
  

