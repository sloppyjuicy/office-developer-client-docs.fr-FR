---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Renvoie un nombre spécifique de caractères d'une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410265"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="08fb8-103">MID Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="08fb8-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="08fb8-104">Renvoie un nombre spécifique de caractères d'une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="08fb8-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="08fb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08fb8-105">Syntax</span></span>

<span data-ttu-id="08fb8-106">MID (\* \* *texte* \* \*, \* \* *no_départ* \* \*, \* \* *no_car* \* \*)</span><span class="sxs-lookup"><span data-stu-id="08fb8-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="08fb8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08fb8-107">Parameters</span></span>

|<span data-ttu-id="08fb8-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="08fb8-108">**Name**</span></span>|<span data-ttu-id="08fb8-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="08fb8-109">**Required/Optional**</span></span>|<span data-ttu-id="08fb8-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="08fb8-110">**Data Type**</span></span>|<span data-ttu-id="08fb8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="08fb8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="08fb8-112">_text_</span><span class="sxs-lookup"><span data-stu-id="08fb8-112">_text_</span></span> <br/> |<span data-ttu-id="08fb8-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="08fb8-113">Required</span></span>  <br/> |<span data-ttu-id="08fb8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="08fb8-114">**String**</span></span> <br/> |<span data-ttu-id="08fb8-115">Chaîne de texte qui contient les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="08fb8-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="08fb8-116">_no_départ_</span><span class="sxs-lookup"><span data-stu-id="08fb8-116">_start_num_</span></span> <br/> |<span data-ttu-id="08fb8-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="08fb8-117">Required</span></span>  <br/> |<span data-ttu-id="08fb8-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="08fb8-118">**Number**</span></span> <br/> |<span data-ttu-id="08fb8-119">Position du premier caractère à extraire.</span><span class="sxs-lookup"><span data-stu-id="08fb8-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="08fb8-120">Le premier caractère de la chaîne de texte est à la position 1.</span><span class="sxs-lookup"><span data-stu-id="08fb8-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="08fb8-121">_no_car_</span><span class="sxs-lookup"><span data-stu-id="08fb8-121">_num_chars_</span></span> <br/> |<span data-ttu-id="08fb8-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="08fb8-122">Required</span></span>  <br/> |<span data-ttu-id="08fb8-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="08fb8-123">**Number**</span></span> <br/> |<span data-ttu-id="08fb8-124">Nombre de caractères à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="08fb8-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="08fb8-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="08fb8-125">Return value</span></span>

<span data-ttu-id="08fb8-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="08fb8-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08fb8-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="08fb8-127">Remarks</span></span>

<span data-ttu-id="08fb8-128">Si *no_départ* est:</span><span class="sxs-lookup"><span data-stu-id="08fb8-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="08fb8-129">Supérieur à la longueur de *Text* , MID renvoie "" (texte vide).</span><span class="sxs-lookup"><span data-stu-id="08fb8-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="08fb8-130">Inférieur à la longueur de *texte* , mais *no_départ* plus *no_car* dépasse la longueur de \*\* texte, MID renvoie les caractères jusqu'à la fin du *texte* .</span><span class="sxs-lookup"><span data-stu-id="08fb8-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="08fb8-131">Inférieur à 1, MID renvoie la #VALUE!</span><span class="sxs-lookup"><span data-stu-id="08fb8-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="08fb8-132">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="08fb8-132">error value.</span></span> 
    
<span data-ttu-id="08fb8-133">Si *no_car* est négatif, MID renvoie la #VALUE!</span><span class="sxs-lookup"><span data-stu-id="08fb8-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="08fb8-134">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="08fb8-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="08fb8-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="08fb8-135">Example</span></span>

<span data-ttu-id="08fb8-136">MID ("SSN 999-99-9999";5;11)</span><span class="sxs-lookup"><span data-stu-id="08fb8-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="08fb8-137">Renvoie 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="08fb8-137">Returns 999-99-9999.</span></span> 
  

