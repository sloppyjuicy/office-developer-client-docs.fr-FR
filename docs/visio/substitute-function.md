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
description: Remplace une partie de chaîne de texte par une autre chaîne de texte.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346822"
---
# <a name="substitute-function"></a><span data-ttu-id="50495-103">Fonction SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="50495-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="50495-104">Remplace une partie de chaîne de texte par une autre chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="50495-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="50495-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50495-105">Syntax</span></span>

 <span data-ttu-id="50495-106">Substitut (\* \* *texte* \* \*, \* \* *ancien_texte* \* \*, \* \* *nouveau_texte* \* \* [, \* \* *no_départ* \* \*] [, \* \* *ignore_case_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="50495-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="50495-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50495-107">Parameters</span></span>

|<span data-ttu-id="50495-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="50495-108">**Name**</span></span>|<span data-ttu-id="50495-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="50495-109">**Required/Optional**</span></span>|<span data-ttu-id="50495-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="50495-110">**Data Type**</span></span>|<span data-ttu-id="50495-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="50495-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="50495-112">_text_</span><span class="sxs-lookup"><span data-stu-id="50495-112">_text_</span></span> <br/> |<span data-ttu-id="50495-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50495-113">Required</span></span>  <br/> |<span data-ttu-id="50495-114">**String**</span><span class="sxs-lookup"><span data-stu-id="50495-114">**String**</span></span> <br/> | <span data-ttu-id="50495-115">Texte ou référence à une cellule contenant le texte dont vous souhaitez substituer des caractères.</span><span class="sxs-lookup"><span data-stu-id="50495-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="50495-116">_ancien_texte_</span><span class="sxs-lookup"><span data-stu-id="50495-116">_old_text_</span></span> <br/> |<span data-ttu-id="50495-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50495-117">Required</span></span>  <br/> |<span data-ttu-id="50495-118">**String**</span><span class="sxs-lookup"><span data-stu-id="50495-118">**String**</span></span> <br/> | <span data-ttu-id="50495-119">Texte à remplacer.</span><span class="sxs-lookup"><span data-stu-id="50495-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="50495-120">_nouveau_texte_</span><span class="sxs-lookup"><span data-stu-id="50495-120">_new_text_</span></span> <br/> |<span data-ttu-id="50495-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50495-121">Required</span></span>  <br/> |<span data-ttu-id="50495-122">**String**</span><span class="sxs-lookup"><span data-stu-id="50495-122">**String**</span></span> <br/> | <span data-ttu-id="50495-123">Texte à utiliser pour remplacer _ancien_texte_.</span><span class="sxs-lookup"><span data-stu-id="50495-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="50495-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="50495-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="50495-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="50495-125">Optional</span></span>  <br/> |<span data-ttu-id="50495-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="50495-126">**Numeric**</span></span> <br/> |<span data-ttu-id="50495-127">Indique les occurrences d'ancien_texte à remplacer.</span><span class="sxs-lookup"><span data-stu-id="50495-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="50495-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="50495-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="50495-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="50495-129">Optional</span></span>  <br/> |<span data-ttu-id="50495-130">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="50495-130">**Boolean**</span></span> <br/> |<span data-ttu-id="50495-131">Valeur FALSE si la casse est respectée ; sinon, valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="50495-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="50495-132">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="50495-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="50495-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50495-133">Return value</span></span>

<span data-ttu-id="50495-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="50495-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50495-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="50495-135">Remarks</span></span>

 <span data-ttu-id="50495-136">Si vous spécifiez _start_num_opt_, seule cette occurrence d' _ancien_texte_ est remplacée.</span><span class="sxs-lookup"><span data-stu-id="50495-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="50495-137">Dans le cas contraire, toutes les occurrences d' _ancien_texte_ dans le _texte_ sont remplacées par _nouveau_texte._</span><span class="sxs-lookup"><span data-stu-id="50495-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="50495-138">Utilisez la fonction SUBSTITUTE lorsque vous souhaitez remplacer un texte spécifique dans une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="50495-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="50495-139">Si vous souhaitez remplacer le texte qui se trouve à un emplacement spécifique dans une chaîne de texte, utilisez la fonction rePLACE.</span><span class="sxs-lookup"><span data-stu-id="50495-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="50495-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="50495-140">Example</span></span>

<span data-ttu-id="50495-141">SUBSTITUTE ("2 janvier 2003", "janvier", "JAN")</span><span class="sxs-lookup"><span data-stu-id="50495-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="50495-142">Renvoie "2 JAN 2003".</span><span class="sxs-lookup"><span data-stu-id="50495-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="50495-143">SUBSTITUTE ("2 janvier 2003","Janvier","JAN")</span><span class="sxs-lookup"><span data-stu-id="50495-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="50495-144">Renvoie "2 janvier 2003".</span><span class="sxs-lookup"><span data-stu-id="50495-144">Returns "1 January 2003".</span></span> <span data-ttu-id="50495-145">Aucune modification n’est apportée car la recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="50495-145">No change is made because the text search is case-sensitive.</span></span> 
  

