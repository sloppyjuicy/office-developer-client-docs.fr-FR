---
title: LOOKUP, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Renvoie un index de base zéro qui indique l’emplacement de la clé de sous-chaîne dans une liste, ou renvoie -1 si la chaîne cible contient le délimiteur.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410328"
---
# <a name="lookup-function"></a><span data-ttu-id="13e7c-103">Fonction LOOKUP</span><span class="sxs-lookup"><span data-stu-id="13e7c-103">LOOKUP Function</span></span>

<span data-ttu-id="13e7c-104">Renvoie un index de base zéro qui indique  l’emplacement de la clé de sous-chaîne dans une _liste,_ ou renvoie -1 si la chaîne cible contient le _délimiteur_.</span><span class="sxs-lookup"><span data-stu-id="13e7c-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="13e7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13e7c-105">Syntax</span></span>

<span data-ttu-id="13e7c-106">LOOKUP( » \*\* *key* \*\* « , » \*\* *list* \*\* « [, » \*\* *delimiter* \*\* « ])</span><span class="sxs-lookup"><span data-stu-id="13e7c-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="13e7c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13e7c-107">Parameters</span></span>

|<span data-ttu-id="13e7c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="13e7c-108">**Name**</span></span>|<span data-ttu-id="13e7c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="13e7c-109">**Required/Optional**</span></span>|<span data-ttu-id="13e7c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="13e7c-110">**Data Type**</span></span>|<span data-ttu-id="13e7c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="13e7c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="13e7c-112">_key_</span><span class="sxs-lookup"><span data-stu-id="13e7c-112">_key_</span></span> <br/> |<span data-ttu-id="13e7c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="13e7c-113">Required</span></span>  <br/> |<span data-ttu-id="13e7c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="13e7c-114">**String**</span></span> <br/> |<span data-ttu-id="13e7c-115">Chaîne à rechercher</span><span class="sxs-lookup"><span data-stu-id="13e7c-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="13e7c-116">_list_</span><span class="sxs-lookup"><span data-stu-id="13e7c-116">_list_</span></span> <br/> |<span data-ttu-id="13e7c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="13e7c-117">Required</span></span>  <br/> |<span data-ttu-id="13e7c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="13e7c-118">**String**</span></span> <br/> | <span data-ttu-id="13e7c-119">Liste dans laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="13e7c-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="13e7c-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="13e7c-120">_delimiter_</span></span> <br/> |<span data-ttu-id="13e7c-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="13e7c-121">Optional</span></span>  <br/> |<span data-ttu-id="13e7c-122">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="13e7c-122">**String**</span></span> <br/> | <span data-ttu-id="13e7c-123">Chaîne à utiliser comme délimiteur dans la _liste._</span><span class="sxs-lookup"><span data-stu-id="13e7c-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="13e7c-124">Une  _chaîne de délimiteur_ peut comporter plusieurs caractères et inclure des caractères multioctets.</span><span class="sxs-lookup"><span data-stu-id="13e7c-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="13e7c-125">La valeur par défaut est le point-virgule.</span><span class="sxs-lookup"><span data-stu-id="13e7c-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="13e7c-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="13e7c-126">Return value</span></span>

<span data-ttu-id="13e7c-127">Numérique</span><span class="sxs-lookup"><span data-stu-id="13e7c-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13e7c-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="13e7c-128">Remarks</span></span>

<span data-ttu-id="13e7c-p102">La fonction LOOKUP ne tient pas compte des majuscules ou des minuscules. Si la liste commence ou finit par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle.</span><span class="sxs-lookup"><span data-stu-id="13e7c-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="13e7c-p103">Tous les arguments doivent être des chaînes ou des expressions qui peuvent être convertis en chaînes. Si la conversion est impossible, une chaîne vide vient remplacer l’argument non accepté.</span><span class="sxs-lookup"><span data-stu-id="13e7c-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="13e7c-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="13e7c-134">Example 1</span></span>

<span data-ttu-id="13e7c-135">LOOKUP(« rat »,"cat;rat;; ; ]</span><span class="sxs-lookup"><span data-stu-id="13e7c-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="13e7c-136">Renvoie 1.</span><span class="sxs-lookup"><span data-stu-id="13e7c-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="13e7c-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="13e7c-137">Example 2</span></span>

<span data-ttu-id="13e7c-138">LOOKUP(«  », »;cat;rat;; ; ]</span><span class="sxs-lookup"><span data-stu-id="13e7c-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="13e7c-139">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="13e7c-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="13e7c-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="13e7c-140">Example 3</span></span>

<span data-ttu-id="13e7c-141">LOOKUP(« t »,"cat;rat;; ; « "a »)</span><span class="sxs-lookup"><span data-stu-id="13e7c-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="13e7c-142">Renvoie 3.</span><span class="sxs-lookup"><span data-stu-id="13e7c-142">Returns 3.</span></span>
  

