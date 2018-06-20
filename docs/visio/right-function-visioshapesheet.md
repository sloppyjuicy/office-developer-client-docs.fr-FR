---
title: Fonction RIGHT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Renvoie l’ou les derniers caractères dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789478"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="04094-103">Fonction RIGHT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="04094-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="04094-104">Renvoie l’ou les derniers caractères dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="04094-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="04094-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04094-105">Syntax</span></span>

<span data-ttu-id="04094-106">DROITE (** *texte* ** [, ** *nb_cars_opt* **])</span><span class="sxs-lookup"><span data-stu-id="04094-106">RIGHT(** *text* ** [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="04094-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04094-107">Parameters</span></span>

|<span data-ttu-id="04094-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="04094-108">**Name**</span></span>|<span data-ttu-id="04094-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="04094-109">**Required/Optional**</span></span>|<span data-ttu-id="04094-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="04094-110">**Data Type**</span></span>|<span data-ttu-id="04094-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="04094-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="04094-112">_text_</span><span class="sxs-lookup"><span data-stu-id="04094-112">_text_</span></span> <br/> |<span data-ttu-id="04094-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="04094-113">Required</span></span>  <br/> |<span data-ttu-id="04094-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="04094-114">**String**</span></span> <br/> | <span data-ttu-id="04094-115">Chaîne de texte contenant les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="04094-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="04094-116">_nb_cars_opt_</span><span class="sxs-lookup"><span data-stu-id="04094-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="04094-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="04094-117">Optional</span></span>  <br/> |<span data-ttu-id="04094-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="04094-118">**Number**</span></span> <br/> |<span data-ttu-id="04094-p101">Nombre de caractères à extraire. La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="04094-p101">The number of characters you want to extract. The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="04094-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="04094-121">Return value</span></span>

<span data-ttu-id="04094-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04094-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04094-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="04094-123">Remarks</span></span>

<span data-ttu-id="04094-124">La valeur de _nb_cars_opt_ doit être supérieure ou égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="04094-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="04094-125">Si _nb_cars_opt_ est supérieur à la longueur du texte, RIGHT renvoie tout le texte.</span><span class="sxs-lookup"><span data-stu-id="04094-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="04094-126">Si _nb_cars_opt_ est omis, il est supposé pour être 1.</span><span class="sxs-lookup"><span data-stu-id="04094-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="04094-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="04094-127">Example</span></span>

<span data-ttu-id="04094-128">RIGHT ("Janvier 1; 2004"; 4)</span><span class="sxs-lookup"><span data-stu-id="04094-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="04094-129">Renvoie la valeur 2004.</span><span class="sxs-lookup"><span data-stu-id="04094-129">Returns the value 2004.</span></span> 
  

