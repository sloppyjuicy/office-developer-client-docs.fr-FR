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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326725"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="744d2-103">RIGHT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="744d2-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="744d2-104">Renvoie le ou les derniers caractères d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="744d2-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="744d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="744d2-105">Syntax</span></span>

<span data-ttu-id="744d2-106">Right (\* \* *texte* \* \* [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="744d2-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="744d2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="744d2-107">Parameters</span></span>

|<span data-ttu-id="744d2-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="744d2-108">**Name**</span></span>|<span data-ttu-id="744d2-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="744d2-109">**Required/Optional**</span></span>|<span data-ttu-id="744d2-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="744d2-110">**Data Type**</span></span>|<span data-ttu-id="744d2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="744d2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="744d2-112">_text_</span><span class="sxs-lookup"><span data-stu-id="744d2-112">_text_</span></span> <br/> |<span data-ttu-id="744d2-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="744d2-113">Required</span></span>  <br/> |<span data-ttu-id="744d2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="744d2-114">**String**</span></span> <br/> | <span data-ttu-id="744d2-115">Chaîne de texte contenant les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="744d2-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="744d2-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="744d2-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="744d2-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="744d2-117">Optional</span></span>  <br/> |<span data-ttu-id="744d2-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="744d2-118">**Number**</span></span> <br/> |<span data-ttu-id="744d2-119">Nombre de caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="744d2-119">The number of characters you want to extract.</span></span> <span data-ttu-id="744d2-120">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="744d2-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="744d2-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="744d2-121">Return value</span></span>

<span data-ttu-id="744d2-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="744d2-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="744d2-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="744d2-123">Remarks</span></span>

<span data-ttu-id="744d2-124">La valeur de _num_chars_opt_ doit être supérieure ou égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="744d2-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="744d2-125">Si _num_chars_opt_ est supérieur à la longueur du texte, Right renvoie tout le texte.</span><span class="sxs-lookup"><span data-stu-id="744d2-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="744d2-126">Si _num_chars_opt_ est omis, il est considéré comme étant égal à 1.</span><span class="sxs-lookup"><span data-stu-id="744d2-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="744d2-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="744d2-127">Example</span></span>

<span data-ttu-id="744d2-128">RIGHT ("Janvier 1; 2004"; 4)</span><span class="sxs-lookup"><span data-stu-id="744d2-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="744d2-129">Renvoie la valeur 2004.</span><span class="sxs-lookup"><span data-stu-id="744d2-129">Returns the value 2004.</span></span> 
  

