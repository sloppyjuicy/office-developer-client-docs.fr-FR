---
title: STRSAMEEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Détermine si deux chaînes sont identiques.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413863"
---
# <a name="strsameex-function"></a><span data-ttu-id="df089-103">Fonction STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="df089-103">STRSAMEEX Function</span></span>

<span data-ttu-id="df089-104">Détermine si deux chaînes sont identiques.</span><span class="sxs-lookup"><span data-stu-id="df089-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="df089-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df089-105">Syntax</span></span>

<span data-ttu-id="df089-106">STRSAMEEX ( » \*\* *string1* \*\* « , " \*\* *string2* \*\* « , \*\* *localeID* \*\*, \*\* *flag* \*\* )</span><span class="sxs-lookup"><span data-stu-id="df089-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df089-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df089-107">Parameters</span></span>

|<span data-ttu-id="df089-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="df089-108">**Name**</span></span>|<span data-ttu-id="df089-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="df089-109">**Required/Optional**</span></span>|<span data-ttu-id="df089-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="df089-110">**Data Type**</span></span>|<span data-ttu-id="df089-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="df089-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df089-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="df089-112">_string1_</span></span> <br/> |<span data-ttu-id="df089-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df089-113">Required</span></span>  <br/> |<span data-ttu-id="df089-114">**String**</span><span class="sxs-lookup"><span data-stu-id="df089-114">**String**</span></span> <br/> |<span data-ttu-id="df089-115">Première chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="df089-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="df089-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="df089-116">_string2_</span></span> <br/> |<span data-ttu-id="df089-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df089-117">Required</span></span>  <br/> |<span data-ttu-id="df089-118">**String**</span><span class="sxs-lookup"><span data-stu-id="df089-118">**String**</span></span> <br/> | <span data-ttu-id="df089-119">Deuxième chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="df089-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="df089-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="df089-120">_localeID_</span></span> <br/> |<span data-ttu-id="df089-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df089-121">Required</span></span>  <br/> |<span data-ttu-id="df089-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="df089-122">**Numeric**</span></span> <br/> |<span data-ttu-id="df089-123">Code du pays (paramètre régional).</span><span class="sxs-lookup"><span data-stu-id="df089-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="df089-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="df089-124">_flag_</span></span> <br/> |<span data-ttu-id="df089-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df089-125">Required</span></span>  <br/> |<span data-ttu-id="df089-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="df089-126">**Numeric**</span></span> <br/> | <span data-ttu-id="df089-127">Bit qui indique le type de comparaison.</span><span class="sxs-lookup"><span data-stu-id="df089-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df089-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df089-128">Return value</span></span>

<span data-ttu-id="df089-129">Booléen</span><span class="sxs-lookup"><span data-stu-id="df089-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df089-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="df089-130">Remarks</span></span>

<span data-ttu-id="df089-131">STRSAMEEX renvoie TRUE si les deux chaînes d’entrée sont identiques et FALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="df089-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="df089-132">Utilisez cette fonction pour comparer des chaînes multi-octets ou pour effectuer des comparaisons qui font appel à des règles de casse pour un paramètre régional spécifique.</span><span class="sxs-lookup"><span data-stu-id="df089-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="df089-133">Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="df089-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="df089-134">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="df089-134">**Flag**</span></span>|<span data-ttu-id="df089-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="df089-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df089-136">1</span><span class="sxs-lookup"><span data-stu-id="df089-136">1</span></span>  <br/> |<span data-ttu-id="df089-137">Ne tient pas compte de la casse.</span><span class="sxs-lookup"><span data-stu-id="df089-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="df089-138">2 </span><span class="sxs-lookup"><span data-stu-id="df089-138">2</span></span>  <br/> |<span data-ttu-id="df089-139">Ne tient pas compte des caractères qui ne définissent pas d’espacement.</span><span class="sxs-lookup"><span data-stu-id="df089-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="df089-140">4 </span><span class="sxs-lookup"><span data-stu-id="df089-140">4</span></span>  <br/> |<span data-ttu-id="df089-141">Ne tient pas compte des symboles.</span><span class="sxs-lookup"><span data-stu-id="df089-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="df089-142">4096</span><span class="sxs-lookup"><span data-stu-id="df089-142">4096</span></span>  <br/> |<span data-ttu-id="df089-143">Traite les signes de ponctuation comme des symboles.</span><span class="sxs-lookup"><span data-stu-id="df089-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="df089-144">65536</span><span class="sxs-lookup"><span data-stu-id="df089-144">65536</span></span>  <br/> |<span data-ttu-id="df089-145">Ne fait aucune différence entre les caractères Hiragana et Katakana.</span><span class="sxs-lookup"><span data-stu-id="df089-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="df089-146">131072</span><span class="sxs-lookup"><span data-stu-id="df089-146">131072</span></span>  <br/> |<span data-ttu-id="df089-147">Ne fait aucune différence entre un caractère codé sur un octet et le même caractère codé sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="df089-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

