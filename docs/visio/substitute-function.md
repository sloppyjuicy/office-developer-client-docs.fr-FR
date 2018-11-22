---
title: SUBSTITUTE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Remplace une partie d’une chaîne de texte avec une autre chaîne de texte.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643212"
---
# <a name="substitute-function"></a><span data-ttu-id="60bb9-103">Fonction SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="60bb9-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="60bb9-104">Remplace une partie d’une chaîne de texte avec une autre chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="60bb9-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="60bb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60bb9-105">Syntax</span></span>

 <span data-ttu-id="60bb9-106">SUBSTITUT (\*\* *texte* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\*] [, \*\* *ignorer_casse_opt* \*\*)</span><span class="sxs-lookup"><span data-stu-id="60bb9-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="60bb9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60bb9-107">Parameters</span></span>

|<span data-ttu-id="60bb9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="60bb9-108">**Name**</span></span>|<span data-ttu-id="60bb9-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="60bb9-109">**Required/Optional**</span></span>|<span data-ttu-id="60bb9-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="60bb9-110">**Data Type**</span></span>|<span data-ttu-id="60bb9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="60bb9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="60bb9-112">_text_</span><span class="sxs-lookup"><span data-stu-id="60bb9-112">_text_</span></span> <br/> |<span data-ttu-id="60bb9-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="60bb9-113">Required</span></span>  <br/> |<span data-ttu-id="60bb9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="60bb9-114">**String**</span></span> <br/> | <span data-ttu-id="60bb9-115">Texte ou référence à une cellule contenant le texte dont vous souhaitez substituer des caractères.</span><span class="sxs-lookup"><span data-stu-id="60bb9-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="60bb9-116">_old_text_</span><span class="sxs-lookup"><span data-stu-id="60bb9-116">_old_text_</span></span> <br/> |<span data-ttu-id="60bb9-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="60bb9-117">Required</span></span>  <br/> |<span data-ttu-id="60bb9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="60bb9-118">**String**</span></span> <br/> | <span data-ttu-id="60bb9-119">Texte à remplacer.
</span><span class="sxs-lookup"><span data-stu-id="60bb9-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="60bb9-120">_new_text_</span><span class="sxs-lookup"><span data-stu-id="60bb9-120">_new_text_</span></span> <br/> |<span data-ttu-id="60bb9-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="60bb9-121">Required</span></span>  <br/> |<span data-ttu-id="60bb9-122">**String**</span><span class="sxs-lookup"><span data-stu-id="60bb9-122">**String**</span></span> <br/> | <span data-ttu-id="60bb9-123">Le texte que vous souhaitez utiliser pour remplacer _old_text_.</span><span class="sxs-lookup"><span data-stu-id="60bb9-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="60bb9-124">_num_début_opt_</span><span class="sxs-lookup"><span data-stu-id="60bb9-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="60bb9-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="60bb9-125">Optional</span></span>  <br/> |<span data-ttu-id="60bb9-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="60bb9-126">**Numeric**</span></span> <br/> |<span data-ttu-id="60bb9-127">Spécifie les occurrences d’old_text à remplacer.</span><span class="sxs-lookup"><span data-stu-id="60bb9-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="60bb9-128">_ignorer_casse_opt_</span><span class="sxs-lookup"><span data-stu-id="60bb9-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="60bb9-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="60bb9-129">Optional</span></span>  <br/> |<span data-ttu-id="60bb9-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="60bb9-130">**Boolean**</span></span> <br/> |<span data-ttu-id="60bb9-p101">Valeur FALSE si la casse est respectée ; sinon, valeur TRUE. La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="60bb9-p101">FALSE if case-sensitive; otherwise, TRUE. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="60bb9-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60bb9-133">Return value</span></span>

<span data-ttu-id="60bb9-134">String</span><span class="sxs-lookup"><span data-stu-id="60bb9-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60bb9-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="60bb9-135">Remarks</span></span>

 <span data-ttu-id="60bb9-136">Si vous spécifiez _num_début_opt_, seule cette occurrence _d’ancien_texte_ est remplacée.</span><span class="sxs-lookup"><span data-stu-id="60bb9-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="60bb9-137">Dans le cas contraire, toutes les occurrences _old_text_ dans le _texte_ sont remplacé par _new_text._</span><span class="sxs-lookup"><span data-stu-id="60bb9-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="60bb9-138">Utilisez la fonction SUBSTITUTE lorsque vous souhaitez remplacer du texte spécifique dans une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="60bb9-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="60bb9-139">Si vous souhaitez remplacer du texte qui se produit dans un emplacement spécifique dans une chaîne de texte, utilisez la fonction REPLACE.</span><span class="sxs-lookup"><span data-stu-id="60bb9-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="60bb9-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="60bb9-140">Example</span></span>

<span data-ttu-id="60bb9-141">SUBSTITUTE ("2 janvier 2003", "janvier", "JAN")</span><span class="sxs-lookup"><span data-stu-id="60bb9-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="60bb9-142">Renvoie "2 JAN 2003".</span><span class="sxs-lookup"><span data-stu-id="60bb9-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="60bb9-143">SUBSTITUTE ("2 janvier 2003","Janvier","JAN")</span><span class="sxs-lookup"><span data-stu-id="60bb9-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="60bb9-144">Renvoie « 1 janvier 2003 ».</span><span class="sxs-lookup"><span data-stu-id="60bb9-144">Returns "1 January 2003".</span></span> <span data-ttu-id="60bb9-145">Aucune modification n’est effectuée, car la recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="60bb9-145">No change is made because the text search is case-sensitive.</span></span> 
  

