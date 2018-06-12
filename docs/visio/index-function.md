---
title: INDEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Retourne la sous-chaîne dans l’index de l’emplacement de base zéro dans la liste délimitée par délimiteur. Ou, si l’index est hors plage, cette propriété renvoie une chaîne vide ou la valeur facultative fournie comme argument errorvalue.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788821"
---
# <a name="index-function"></a><span data-ttu-id="a455d-104">INDEX, fonction</span><span class="sxs-lookup"><span data-stu-id="a455d-104">INDEX Function</span></span>

<span data-ttu-id="a455d-105">Retourne la sous-chaîne à l' emplacement de base zéro _index_ dans la _liste_ délimitée par _délimiteur_.</span><span class="sxs-lookup"><span data-stu-id="a455d-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="a455d-106">Ou, si l’index est hors plage, cette propriété renvoie une chaîne vide ou la valeur facultative fournie comme argument *errorvalue* .</span><span class="sxs-lookup"><span data-stu-id="a455d-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a455d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a455d-107">Syntax</span></span>

<span data-ttu-id="a455d-108">INDEX (** *index* **, « ** *liste* ** » [, [** *délimiteur* **] [, [** *errorvalue* **]]])</span><span class="sxs-lookup"><span data-stu-id="a455d-108">INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a455d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a455d-109">Parameters</span></span>

|<span data-ttu-id="a455d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a455d-110">**Name**</span></span>|<span data-ttu-id="a455d-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a455d-111">**Required/Optional**</span></span>|<span data-ttu-id="a455d-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a455d-112">**Data Type**</span></span>|<span data-ttu-id="a455d-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="a455d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a455d-114">_index_</span><span class="sxs-lookup"><span data-stu-id="a455d-114">_index_</span></span> <br/> |<span data-ttu-id="a455d-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a455d-115">Required</span></span>  <br/> |<span data-ttu-id="a455d-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="a455d-116">**Number**</span></span> <br/> |<span data-ttu-id="a455d-117">Emplacement à localiser.</span><span class="sxs-lookup"><span data-stu-id="a455d-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="a455d-118">_liste_</span><span class="sxs-lookup"><span data-stu-id="a455d-118">_list_</span></span> <br/> |<span data-ttu-id="a455d-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a455d-119">Required</span></span>  <br/> |<span data-ttu-id="a455d-120">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a455d-120">**String**</span></span> <br/> |<span data-ttu-id="a455d-121">Liste dans laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="a455d-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="a455d-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="a455d-122">_delimiter_</span></span> <br/> |<span data-ttu-id="a455d-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a455d-123">Optional</span></span>  <br/> |<span data-ttu-id="a455d-124">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a455d-124">**String**</span></span> <br/> | <span data-ttu-id="a455d-125">La chaîne à utiliser comme délimiteur dans la _liste_.</span><span class="sxs-lookup"><span data-stu-id="a455d-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="a455d-126">Une chaîne de _délimiteur_ peut comporter plusieurs caractères et inclure des caractères codés.</span><span class="sxs-lookup"><span data-stu-id="a455d-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="a455d-127">La valeur par défaut est un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="a455d-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="a455d-128">_ERRORVALUE_</span><span class="sxs-lookup"><span data-stu-id="a455d-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="a455d-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a455d-129">Optional</span></span>  <br/> |<span data-ttu-id="a455d-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="a455d-130">**Number**</span></span> <br/> | <span data-ttu-id="a455d-p104">Valeur définie par l’utilisateur renvoyée si l’index est hors des limites admises. La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="a455d-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a455d-133">Note</span><span class="sxs-lookup"><span data-stu-id="a455d-133">Remarks</span></span>

<span data-ttu-id="a455d-p105">Si la liste commence ou se termine par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle.</span><span class="sxs-lookup"><span data-stu-id="a455d-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="a455d-136">Si l’index est hors limites, Visio renvoie une chaîne vide ou la valeur facultative fournie comme argument *errorvalue* .</span><span class="sxs-lookup"><span data-stu-id="a455d-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a455d-137">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a455d-137">Example 1</span></span>

<span data-ttu-id="a455d-138">INDEX(3,"chat;rat;;chèvre")</span><span class="sxs-lookup"><span data-stu-id="a455d-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="a455d-139">Renvoie « chèvre ».</span><span class="sxs-lookup"><span data-stu-id="a455d-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a455d-140">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a455d-140">Example 2</span></span>

<span data-ttu-id="a455d-141">INDEX(54,";1;2;3;",,"ERREUR")</span><span class="sxs-lookup"><span data-stu-id="a455d-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="a455d-142">Renvoie « Erreur ».</span><span class="sxs-lookup"><span data-stu-id="a455d-142">Returns "ERROR".</span></span>
  

