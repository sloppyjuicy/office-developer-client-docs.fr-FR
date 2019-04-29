---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Renvoie le ou les derniers caractères d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411455"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="4c665-103">RIGHT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4c665-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4c665-104">Renvoie le ou les derniers caractères d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="4c665-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4c665-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c665-105">Syntax</span></span>

<span data-ttu-id="4c665-106">Right (\* \* *texte* \* \* [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="4c665-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4c665-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c665-107">Parameters</span></span>

|<span data-ttu-id="4c665-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4c665-108">**Name**</span></span>|<span data-ttu-id="4c665-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="4c665-109">**Required/Optional**</span></span>|<span data-ttu-id="4c665-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="4c665-110">**Data Type**</span></span>|<span data-ttu-id="4c665-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c665-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4c665-112">_text_</span><span class="sxs-lookup"><span data-stu-id="4c665-112">_text_</span></span> <br/> |<span data-ttu-id="4c665-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c665-113">Required</span></span>  <br/> |<span data-ttu-id="4c665-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4c665-114">**String**</span></span> <br/> | <span data-ttu-id="4c665-115">Chaîne de texte contenant les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="4c665-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="4c665-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="4c665-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="4c665-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="4c665-117">Optional</span></span>  <br/> |<span data-ttu-id="4c665-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="4c665-118">**Number**</span></span> <br/> |<span data-ttu-id="4c665-119">Nombre de caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="4c665-119">The number of characters you want to extract.</span></span> <span data-ttu-id="4c665-120">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="4c665-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4c665-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c665-121">Return value</span></span>

<span data-ttu-id="4c665-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4c665-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c665-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c665-123">Remarks</span></span>

<span data-ttu-id="4c665-124">La valeur de _num_chars_opt_ doit être supérieure ou égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="4c665-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="4c665-125">Si _num_chars_opt_ est supérieur à la longueur du texte, Right renvoie tout le texte.</span><span class="sxs-lookup"><span data-stu-id="4c665-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="4c665-126">Si _num_chars_opt_ est omis, il est considéré comme étant égal à 1.</span><span class="sxs-lookup"><span data-stu-id="4c665-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4c665-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c665-127">Example</span></span>

<span data-ttu-id="4c665-128">RIGHT ("Janvier 1; 2004"; 4)</span><span class="sxs-lookup"><span data-stu-id="4c665-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="4c665-129">Renvoie la valeur 2004.</span><span class="sxs-lookup"><span data-stu-id="4c665-129">Returns the value 2004.</span></span> 
  

