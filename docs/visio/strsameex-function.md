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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329791"
---
# <a name="strsameex-function"></a><span data-ttu-id="6d221-103">Fonction STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="6d221-103">STRSAMEEX Function</span></span>

<span data-ttu-id="6d221-104">Détermine si deux chaînes sont identiques.</span><span class="sxs-lookup"><span data-stu-id="6d221-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6d221-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d221-105">Syntax</span></span>

<span data-ttu-id="6d221-106">STRSAMEEX ("\* \* *Chaîne1* \* *", "* \* *Chaîne2* \* \*", \* \* *LocaleID* \* \*, \* \* *indicateur* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6d221-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6d221-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d221-107">Parameters</span></span>

|<span data-ttu-id="6d221-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6d221-108">**Name**</span></span>|<span data-ttu-id="6d221-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="6d221-109">**Required/Optional**</span></span>|<span data-ttu-id="6d221-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="6d221-110">**Data Type**</span></span>|<span data-ttu-id="6d221-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="6d221-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6d221-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="6d221-112">_string1_</span></span> <br/> |<span data-ttu-id="6d221-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d221-113">Required</span></span>  <br/> |<span data-ttu-id="6d221-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6d221-114">**String**</span></span> <br/> |<span data-ttu-id="6d221-115">Première chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="6d221-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="6d221-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="6d221-116">_string2_</span></span> <br/> |<span data-ttu-id="6d221-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d221-117">Required</span></span>  <br/> |<span data-ttu-id="6d221-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6d221-118">**String**</span></span> <br/> | <span data-ttu-id="6d221-119">Deuxième chaîne à comparer.</span><span class="sxs-lookup"><span data-stu-id="6d221-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="6d221-120">_Régionaux_</span><span class="sxs-lookup"><span data-stu-id="6d221-120">_localeID_</span></span> <br/> |<span data-ttu-id="6d221-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d221-121">Required</span></span>  <br/> |<span data-ttu-id="6d221-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="6d221-122">**Numeric**</span></span> <br/> |<span data-ttu-id="6d221-123">Code du pays (paramètre régional).</span><span class="sxs-lookup"><span data-stu-id="6d221-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="6d221-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="6d221-124">_flag_</span></span> <br/> |<span data-ttu-id="6d221-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d221-125">Required</span></span>  <br/> |<span data-ttu-id="6d221-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="6d221-126">**Numeric**</span></span> <br/> | <span data-ttu-id="6d221-127">Bit qui indique le type de comparaison.</span><span class="sxs-lookup"><span data-stu-id="6d221-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6d221-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d221-128">Return value</span></span>

<span data-ttu-id="6d221-129">Booléen</span><span class="sxs-lookup"><span data-stu-id="6d221-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d221-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d221-130">Remarks</span></span>

<span data-ttu-id="6d221-131">STRSAMEEX renvoie TRUE si les deux chaînes d’entrée sont identiques et FALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6d221-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="6d221-132">Utilisez cette fonction pour comparer des chaînes multi-octets ou pour effectuer des comparaisons qui font appel à des règles de casse pour un paramètre régional spécifique.</span><span class="sxs-lookup"><span data-stu-id="6d221-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="6d221-133">Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="6d221-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="6d221-134">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="6d221-134">**Flag**</span></span>|<span data-ttu-id="6d221-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="6d221-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d221-136">0,1</span><span class="sxs-lookup"><span data-stu-id="6d221-136">1</span></span>  <br/> |<span data-ttu-id="6d221-137">Ne tient pas compte de la casse.</span><span class="sxs-lookup"><span data-stu-id="6d221-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="6d221-138">n°2</span><span class="sxs-lookup"><span data-stu-id="6d221-138">2</span></span>  <br/> |<span data-ttu-id="6d221-139">Ne tient pas compte des caractères qui ne définissent pas d’espacement.</span><span class="sxs-lookup"><span data-stu-id="6d221-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="6d221-140">4</span><span class="sxs-lookup"><span data-stu-id="6d221-140">4</span></span>  <br/> |<span data-ttu-id="6d221-141">Ne tient pas compte des symboles.</span><span class="sxs-lookup"><span data-stu-id="6d221-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="6d221-142">4096</span><span class="sxs-lookup"><span data-stu-id="6d221-142">4096</span></span>  <br/> |<span data-ttu-id="6d221-143">Traite les signes de ponctuation comme des symboles.</span><span class="sxs-lookup"><span data-stu-id="6d221-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="6d221-144">65536</span><span class="sxs-lookup"><span data-stu-id="6d221-144">65536</span></span>  <br/> |<span data-ttu-id="6d221-145">Ne fait aucune différence entre les caractères Hiragana et Katakana.</span><span class="sxs-lookup"><span data-stu-id="6d221-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="6d221-146">131072</span><span class="sxs-lookup"><span data-stu-id="6d221-146">131072</span></span>  <br/> |<span data-ttu-id="6d221-147">Ne fait aucune différence entre un caractère codé sur un octet et le même caractère codé sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="6d221-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

