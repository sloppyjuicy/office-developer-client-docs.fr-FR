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
description: Détermine si les deux chaînes sont identiques.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789835"
---
# <a name="strsameex-function"></a><span data-ttu-id="f67e8-103">STRSAMEEX, fonction</span><span class="sxs-lookup"><span data-stu-id="f67e8-103">STRSAMEEX Function</span></span>

<span data-ttu-id="f67e8-104">Détermine si les deux chaînes sont identiques.</span><span class="sxs-lookup"><span data-stu-id="f67e8-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f67e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f67e8-105">Syntax</span></span>

<span data-ttu-id="f67e8-106">STRSAMEEX (« ** *chaîne1* ** «, » ** *chaîne2* ** », ** *localeID* **, ** *indicateur* **)</span><span class="sxs-lookup"><span data-stu-id="f67e8-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f67e8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f67e8-107">Parameters</span></span>

|<span data-ttu-id="f67e8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f67e8-108">**Name**</span></span>|<span data-ttu-id="f67e8-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f67e8-109">**Required/Optional**</span></span>|<span data-ttu-id="f67e8-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f67e8-110">**Data Type**</span></span>|<span data-ttu-id="f67e8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f67e8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f67e8-112">_chaîne string1_</span><span class="sxs-lookup"><span data-stu-id="f67e8-112">_string1_</span></span> <br/> |<span data-ttu-id="f67e8-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f67e8-113">Required</span></span>  <br/> |<span data-ttu-id="f67e8-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="f67e8-114">**String**</span></span> <br/> |<span data-ttu-id="f67e8-115">Première chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="f67e8-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="f67e8-116">_chaîne2_</span><span class="sxs-lookup"><span data-stu-id="f67e8-116">_string2_</span></span> <br/> |<span data-ttu-id="f67e8-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f67e8-117">Required</span></span>  <br/> |<span data-ttu-id="f67e8-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="f67e8-118">**String**</span></span> <br/> | <span data-ttu-id="f67e8-119">Deuxième chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="f67e8-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="f67e8-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="f67e8-120">_localeID_</span></span> <br/> |<span data-ttu-id="f67e8-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f67e8-121">Required</span></span>  <br/> |<span data-ttu-id="f67e8-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="f67e8-122">**Numeric**</span></span> <br/> |<span data-ttu-id="f67e8-123">Code du pays (paramètre régional).</span><span class="sxs-lookup"><span data-stu-id="f67e8-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="f67e8-124">_indicateur_</span><span class="sxs-lookup"><span data-stu-id="f67e8-124">_flag_</span></span> <br/> |<span data-ttu-id="f67e8-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f67e8-125">Required</span></span>  <br/> |<span data-ttu-id="f67e8-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="f67e8-126">**Numeric**</span></span> <br/> | <span data-ttu-id="f67e8-127">Bit qui indique le type de comparaison.</span><span class="sxs-lookup"><span data-stu-id="f67e8-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f67e8-128">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f67e8-128">Return value</span></span>

<span data-ttu-id="f67e8-129">Booléenne</span><span class="sxs-lookup"><span data-stu-id="f67e8-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f67e8-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="f67e8-130">Remarks</span></span>

<span data-ttu-id="f67e8-131">STRSAMEEX renvoie TRUE si les deux chaînes d’entrée sont identiques et FALSE si elles ne sont pas.</span><span class="sxs-lookup"><span data-stu-id="f67e8-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="f67e8-132">Utilisez cette fonction pour comparer des chaînes multi-octets ou pour effectuer des comparaisons qui utilisent des règles de casse pour un paramètre régional spécifique.</span><span class="sxs-lookup"><span data-stu-id="f67e8-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="f67e8-133">Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="f67e8-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="f67e8-134">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="f67e8-134">**Flag**</span></span>|<span data-ttu-id="f67e8-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="f67e8-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f67e8-136">1</span><span class="sxs-lookup"><span data-stu-id="f67e8-136">1</span></span>  <br/> |<span data-ttu-id="f67e8-137">Ne tient pas compte de la casse.</span><span class="sxs-lookup"><span data-stu-id="f67e8-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="f67e8-138">2</span><span class="sxs-lookup"><span data-stu-id="f67e8-138">2</span></span>  <br/> |<span data-ttu-id="f67e8-139">Ne tient pas compte des caractères qui ne définissent pas d’espacement.</span><span class="sxs-lookup"><span data-stu-id="f67e8-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="f67e8-140">4</span><span class="sxs-lookup"><span data-stu-id="f67e8-140">4</span></span>  <br/> |<span data-ttu-id="f67e8-141">Ne tient pas compte des symboles.</span><span class="sxs-lookup"><span data-stu-id="f67e8-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="f67e8-142">4096</span><span class="sxs-lookup"><span data-stu-id="f67e8-142">4096</span></span>  <br/> |<span data-ttu-id="f67e8-143">Traite les signes de ponctuation comme des symboles.</span><span class="sxs-lookup"><span data-stu-id="f67e8-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="f67e8-144">65536</span><span class="sxs-lookup"><span data-stu-id="f67e8-144">65536</span></span>  <br/> |<span data-ttu-id="f67e8-145">Ne fait aucune différence entre les caractères Hiragana et Katakana.</span><span class="sxs-lookup"><span data-stu-id="f67e8-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="f67e8-146">131072</span><span class="sxs-lookup"><span data-stu-id="f67e8-146">131072</span></span>  <br/> |<span data-ttu-id="f67e8-147">Ne fait aucune différence entre un caractère codé sur un octet et le même caractère codé sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="f67e8-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

