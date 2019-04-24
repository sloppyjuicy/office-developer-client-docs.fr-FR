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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360661"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="fb4ec-103">MID Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fb4ec-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fb4ec-104">Renvoie un nombre spécifique de caractères d'une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fb4ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb4ec-105">Syntax</span></span>

<span data-ttu-id="fb4ec-106">MID (\* \* *texte* \* \*, \* \* *no_départ* \* \*, \* \* *no_car* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fb4ec-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fb4ec-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb4ec-107">Parameters</span></span>

|<span data-ttu-id="fb4ec-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-108">**Name**</span></span>|<span data-ttu-id="fb4ec-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-109">**Required/Optional**</span></span>|<span data-ttu-id="fb4ec-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-110">**Data Type**</span></span>|<span data-ttu-id="fb4ec-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fb4ec-112">_text_</span><span class="sxs-lookup"><span data-stu-id="fb4ec-112">_text_</span></span> <br/> |<span data-ttu-id="fb4ec-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fb4ec-113">Required</span></span>  <br/> |<span data-ttu-id="fb4ec-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-114">**String**</span></span> <br/> |<span data-ttu-id="fb4ec-115">Chaîne de texte qui contient les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="fb4ec-116">_no_départ_</span><span class="sxs-lookup"><span data-stu-id="fb4ec-116">_start_num_</span></span> <br/> |<span data-ttu-id="fb4ec-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fb4ec-117">Required</span></span>  <br/> |<span data-ttu-id="fb4ec-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-118">**Number**</span></span> <br/> |<span data-ttu-id="fb4ec-119">Position du premier caractère à extraire.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="fb4ec-120">Le premier caractère de la chaîne de texte est à la position 1.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="fb4ec-121">_no_car_</span><span class="sxs-lookup"><span data-stu-id="fb4ec-121">_num_chars_</span></span> <br/> |<span data-ttu-id="fb4ec-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fb4ec-122">Required</span></span>  <br/> |<span data-ttu-id="fb4ec-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="fb4ec-123">**Number**</span></span> <br/> |<span data-ttu-id="fb4ec-124">Nombre de caractères à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fb4ec-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fb4ec-125">Return value</span></span>

<span data-ttu-id="fb4ec-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="fb4ec-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb4ec-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb4ec-127">Remarks</span></span>

<span data-ttu-id="fb4ec-128">Si *no_départ* est:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="fb4ec-129">Supérieur à la longueur de *Text* , MID renvoie "" (texte vide).</span><span class="sxs-lookup"><span data-stu-id="fb4ec-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="fb4ec-130">Inférieur à la longueur de *texte* , mais *no_départ* plus *no_car* dépasse la longueur de \*\* texte, MID renvoie les caractères jusqu'à la fin du *texte* .</span><span class="sxs-lookup"><span data-stu-id="fb4ec-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="fb4ec-131">Inférieur à 1, MID renvoie la #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fb4ec-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="fb4ec-132">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-132">error value.</span></span> 
    
<span data-ttu-id="fb4ec-133">Si *no_car* est négatif, MID renvoie la #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fb4ec-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="fb4ec-134">Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fb4ec-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb4ec-135">Example</span></span>

<span data-ttu-id="fb4ec-136">MID ("SSN 999-99-9999";5;11)</span><span class="sxs-lookup"><span data-stu-id="fb4ec-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="fb4ec-137">Renvoie 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-137">Returns 999-99-9999.</span></span> 
  

