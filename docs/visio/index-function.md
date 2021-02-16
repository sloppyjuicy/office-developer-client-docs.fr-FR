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
description: Renvoie la sous-stration à l’index d’emplacement de base zéro dans la liste délimitée par le délimiteur. Ou, si l’index est en dehors de la plage, renvoie une chaîne vide ou le jeton facultatif fourni en tant qu’argument valeur d’erreur.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431574"
---
# <a name="index-function"></a><span data-ttu-id="61627-104">Fonction INDEX</span><span class="sxs-lookup"><span data-stu-id="61627-104">INDEX Function</span></span>

<span data-ttu-id="61627-105">Renvoie la sous-stration à  _l’index_ d’emplacement de base zéro dans la  _liste_ délimitée par  _le délimiteur_.</span><span class="sxs-lookup"><span data-stu-id="61627-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="61627-106">Ou, si l’index est en dehors de la plage, renvoie une chaîne vide ou le jeton facultatif fourni en tant qu’argument *valeur d’erreur.*</span><span class="sxs-lookup"><span data-stu-id="61627-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61627-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61627-107">Syntax</span></span>

<span data-ttu-id="61627-108">INDEX(\*\* *index* \*\*, » \*\* *list* \*\* « [,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span><span class="sxs-lookup"><span data-stu-id="61627-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61627-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61627-109">Parameters</span></span>

|<span data-ttu-id="61627-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="61627-110">**Name**</span></span>|<span data-ttu-id="61627-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="61627-111">**Required/Optional**</span></span>|<span data-ttu-id="61627-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="61627-112">**Data Type**</span></span>|<span data-ttu-id="61627-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="61627-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61627-114">_index_</span><span class="sxs-lookup"><span data-stu-id="61627-114">_index_</span></span> <br/> |<span data-ttu-id="61627-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="61627-115">Required</span></span>  <br/> |<span data-ttu-id="61627-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="61627-116">**Number**</span></span> <br/> |<span data-ttu-id="61627-117">Emplacement à localiser.</span><span class="sxs-lookup"><span data-stu-id="61627-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="61627-118">_list_</span><span class="sxs-lookup"><span data-stu-id="61627-118">_list_</span></span> <br/> |<span data-ttu-id="61627-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="61627-119">Required</span></span>  <br/> |<span data-ttu-id="61627-120">**String**</span><span class="sxs-lookup"><span data-stu-id="61627-120">**String**</span></span> <br/> |<span data-ttu-id="61627-121">Liste dans laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="61627-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="61627-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="61627-122">_delimiter_</span></span> <br/> |<span data-ttu-id="61627-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="61627-123">Optional</span></span>  <br/> |<span data-ttu-id="61627-124">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="61627-124">**String**</span></span> <br/> | <span data-ttu-id="61627-125">Chaîne à utiliser comme délimiteur dans la _liste._</span><span class="sxs-lookup"><span data-stu-id="61627-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="61627-126">Une  _chaîne de délimiteur_ peut comporter plusieurs caractères et inclure des caractères à plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="61627-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="61627-127">La valeur par défaut est le point-virgule.</span><span class="sxs-lookup"><span data-stu-id="61627-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="61627-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="61627-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="61627-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="61627-129">Optional</span></span>  <br/> |<span data-ttu-id="61627-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="61627-130">**Number**</span></span> <br/> | <span data-ttu-id="61627-131">Valeur définie par l’utilisateur renvoyée si l’index est hors des limites admises.</span><span class="sxs-lookup"><span data-stu-id="61627-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="61627-132">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="61627-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61627-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="61627-133">Remarks</span></span>

<span data-ttu-id="61627-p105">Si la liste commence ou se termine par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle.</span><span class="sxs-lookup"><span data-stu-id="61627-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="61627-136">Si l’index est hors de portée, Visio renvoie une chaîne vide ou le jeton facultatif fourni en tant qu’argument *valeur d’erreur.*</span><span class="sxs-lookup"><span data-stu-id="61627-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="61627-137">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="61627-137">Example 1</span></span>

<span data-ttu-id="61627-138">INDEX(3,"cat;rat;; ; ]</span><span class="sxs-lookup"><span data-stu-id="61627-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="61627-139">Renvoie « chèvre ».</span><span class="sxs-lookup"><span data-stu-id="61627-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="61627-140">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="61627-140">Example 2</span></span>

<span data-ttu-id="61627-141">INDEX(54, »;1;2;3; »,,"ERROR »)</span><span class="sxs-lookup"><span data-stu-id="61627-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="61627-142">Renvoie « ERROR ».</span><span class="sxs-lookup"><span data-stu-id="61627-142">Returns "ERROR".</span></span>
  

