---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Renvoie le ou les caractères les plus à gauche d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309463"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="d2f7b-103">LEFT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d2f7b-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d2f7b-104">Renvoie le ou les caractères les plus à gauche d'une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="d2f7b-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d2f7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f7b-105">Syntax</span></span>

<span data-ttu-id="d2f7b-106">Gauche (\* \* *texte* \* \*, [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="d2f7b-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d2f7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2f7b-107">Parameters</span></span>

|<span data-ttu-id="d2f7b-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d2f7b-108">**Name**</span></span>|<span data-ttu-id="d2f7b-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d2f7b-109">**Required/Optional**</span></span>|<span data-ttu-id="d2f7b-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d2f7b-110">**Data Type**</span></span>|<span data-ttu-id="d2f7b-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2f7b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d2f7b-112">_text_</span><span class="sxs-lookup"><span data-stu-id="d2f7b-112">_text_</span></span> <br/> |<span data-ttu-id="d2f7b-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d2f7b-113">Required</span></span>  <br/> |<span data-ttu-id="d2f7b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d2f7b-114">**String**</span></span> <br/> |<span data-ttu-id="d2f7b-115">Chaîne de texte qui contient les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="d2f7b-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="d2f7b-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="d2f7b-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="d2f7b-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d2f7b-117">Optional</span></span>  <br/> |<span data-ttu-id="d2f7b-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="d2f7b-118">**Numeric**</span></span> <br/> |<span data-ttu-id="d2f7b-119">Nombre de caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="d2f7b-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d2f7b-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2f7b-120">Return value</span></span>

<span data-ttu-id="d2f7b-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d2f7b-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2f7b-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2f7b-122">Remarks</span></span>

<span data-ttu-id="d2f7b-123">La valeur de _num_chars_opt_ doit être supérieure ou égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d2f7b-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="d2f7b-124">Si _num_chars_opt_ est supérieur à la longueur du texte, Left renvoie tout le texte.</span><span class="sxs-lookup"><span data-stu-id="d2f7b-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="d2f7b-125">Si _num_chars_opt_ est omis, il est considéré comme étant égal à 1.</span><span class="sxs-lookup"><span data-stu-id="d2f7b-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d2f7b-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2f7b-126">Example</span></span>

<span data-ttu-id="d2f7b-127">LEFT ("Janvier 1 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="d2f7b-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="d2f7b-128">Renvoie la valeur "Jan".</span><span class="sxs-lookup"><span data-stu-id="d2f7b-128">Returns the value "Jan".</span></span> 
  

