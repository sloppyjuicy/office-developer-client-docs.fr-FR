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
description: Répète le texte un certain nombre de fois.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326802"
---
# <a name="rept-function"></a><span data-ttu-id="33ecf-103">Fonction REPT</span><span class="sxs-lookup"><span data-stu-id="33ecf-103">REPT Function</span></span>

<span data-ttu-id="33ecf-104">Répète le texte un certain nombre de fois.</span><span class="sxs-lookup"><span data-stu-id="33ecf-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="33ecf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33ecf-105">Syntax</span></span>

<span data-ttu-id="33ecf-106">REPT (\* \* *texte* \* \*, \* \* *no_fois* \* \*)</span><span class="sxs-lookup"><span data-stu-id="33ecf-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="33ecf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33ecf-107">Parameters</span></span>

|<span data-ttu-id="33ecf-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="33ecf-108">**Name**</span></span>|<span data-ttu-id="33ecf-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="33ecf-109">**Required/Optional**</span></span>|<span data-ttu-id="33ecf-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="33ecf-110">**Data Type**</span></span>|<span data-ttu-id="33ecf-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="33ecf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="33ecf-112">_text_</span><span class="sxs-lookup"><span data-stu-id="33ecf-112">_text_</span></span> <br/> |<span data-ttu-id="33ecf-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="33ecf-113">Required</span></span>  <br/> |<span data-ttu-id="33ecf-114">**String**</span><span class="sxs-lookup"><span data-stu-id="33ecf-114">**String**</span></span> <br/> | <span data-ttu-id="33ecf-115">Texte à répéter.</span><span class="sxs-lookup"><span data-stu-id="33ecf-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="33ecf-116">_no_fois_</span><span class="sxs-lookup"><span data-stu-id="33ecf-116">_number_times_</span></span> <br/> |<span data-ttu-id="33ecf-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="33ecf-117">Required</span></span>  <br/> |<span data-ttu-id="33ecf-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="33ecf-118">**Number**</span></span> <br/> |<span data-ttu-id="33ecf-119">Valeur positive spécifiant le nombre de fois que le texte doit être répété.</span><span class="sxs-lookup"><span data-stu-id="33ecf-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33ecf-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="33ecf-120">Remarks</span></span>

<span data-ttu-id="33ecf-121">Si *no_fois* est:</span><span class="sxs-lookup"><span data-stu-id="33ecf-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="33ecf-122">est zéro (0), REPT renvoie "" (texte vide) ;</span><span class="sxs-lookup"><span data-stu-id="33ecf-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="33ecf-123">n’est pas un entier, il est tronqué.</span><span class="sxs-lookup"><span data-stu-id="33ecf-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="33ecf-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="33ecf-124">Example</span></span>

<span data-ttu-id="33ecf-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="33ecf-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="33ecf-126">\* \*Renvoie \*. \* \*</span><span class="sxs-lookup"><span data-stu-id="33ecf-126">Returns \*\*\*\*\*.</span></span> 
  

