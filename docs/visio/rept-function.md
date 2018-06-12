---
title: REPT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Répète un texte un certain nombre de fois.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789497"
---
# <a name="rept-function"></a><span data-ttu-id="0b86e-103">REPT, fonction</span><span class="sxs-lookup"><span data-stu-id="0b86e-103">REPT Function</span></span>

<span data-ttu-id="0b86e-104">Répète un texte un certain nombre de fois.</span><span class="sxs-lookup"><span data-stu-id="0b86e-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0b86e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b86e-105">Syntax</span></span>

<span data-ttu-id="0b86e-106">REPT (** *texte* **, ** *number_times* **)</span><span class="sxs-lookup"><span data-stu-id="0b86e-106">REPT (** *text* **, ** *number_times* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0b86e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b86e-107">Parameters</span></span>

|<span data-ttu-id="0b86e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="0b86e-108">**Name**</span></span>|<span data-ttu-id="0b86e-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0b86e-109">**Required/Optional**</span></span>|<span data-ttu-id="0b86e-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0b86e-110">**Data Type**</span></span>|<span data-ttu-id="0b86e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="0b86e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0b86e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="0b86e-112">_text_</span></span> <br/> |<span data-ttu-id="0b86e-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0b86e-113">Required</span></span>  <br/> |<span data-ttu-id="0b86e-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="0b86e-114">**String**</span></span> <br/> | <span data-ttu-id="0b86e-115">Texte à répéter.</span><span class="sxs-lookup"><span data-stu-id="0b86e-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="0b86e-116">_number_times_</span><span class="sxs-lookup"><span data-stu-id="0b86e-116">_number_times_</span></span> <br/> |<span data-ttu-id="0b86e-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0b86e-117">Required</span></span>  <br/> |<span data-ttu-id="0b86e-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="0b86e-118">**Number**</span></span> <br/> |<span data-ttu-id="0b86e-119">Valeur positive spécifiant le nombre de fois que le texte doit être répété.</span><span class="sxs-lookup"><span data-stu-id="0b86e-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b86e-120">Note</span><span class="sxs-lookup"><span data-stu-id="0b86e-120">Remarks</span></span>

<span data-ttu-id="0b86e-121">Si *number_times :*</span><span class="sxs-lookup"><span data-stu-id="0b86e-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="0b86e-122">est zéro (0), REPT renvoie "" (texte vide) ;</span><span class="sxs-lookup"><span data-stu-id="0b86e-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="0b86e-123">n’est pas un entier, il est tronqué.</span><span class="sxs-lookup"><span data-stu-id="0b86e-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="0b86e-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="0b86e-124">Example</span></span>

<span data-ttu-id="0b86e-125">REPT («\*», 5)</span><span class="sxs-lookup"><span data-stu-id="0b86e-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="0b86e-126">Cette propriété renvoie \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="0b86e-126">Returns \*\*\*\*\*.</span></span> 
  

