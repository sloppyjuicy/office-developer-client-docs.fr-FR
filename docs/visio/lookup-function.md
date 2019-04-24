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
description: Renvoie un index de base zéro qui indique l'emplacement de la clé de sous-chaîne dans une liste ou renvoie-1 si la chaîne cible contient le délimiteur.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358029"
---
# <a name="lookup-function"></a><span data-ttu-id="e376e-103">Fonction LOOKUP</span><span class="sxs-lookup"><span data-stu-id="e376e-103">LOOKUP Function</span></span>

<span data-ttu-id="e376e-104">Renvoie un index de base zéro qui indique l'emplacement de la _clé_ de sous-chaîne dans une _liste_ou renvoie-1 si la chaîne cible contient __ le délimiteur.</span><span class="sxs-lookup"><span data-stu-id="e376e-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e376e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e376e-105">Syntax</span></span>

<span data-ttu-id="e376e-106">Lookup ("\* \* *Key* \* *", "* \* *List* \* *" [, "* \* \*\* délimiteur \* \*"])</span><span class="sxs-lookup"><span data-stu-id="e376e-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e376e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e376e-107">Parameters</span></span>

|<span data-ttu-id="e376e-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e376e-108">**Name**</span></span>|<span data-ttu-id="e376e-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e376e-109">**Required/Optional**</span></span>|<span data-ttu-id="e376e-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e376e-110">**Data Type**</span></span>|<span data-ttu-id="e376e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e376e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e376e-112">_key_</span><span class="sxs-lookup"><span data-stu-id="e376e-112">_key_</span></span> <br/> |<span data-ttu-id="e376e-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e376e-113">Required</span></span>  <br/> |<span data-ttu-id="e376e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e376e-114">**String**</span></span> <br/> |<span data-ttu-id="e376e-115">Chaîne à rechercher</span><span class="sxs-lookup"><span data-stu-id="e376e-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="e376e-116">_liste_</span><span class="sxs-lookup"><span data-stu-id="e376e-116">_list_</span></span> <br/> |<span data-ttu-id="e376e-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e376e-117">Required</span></span>  <br/> |<span data-ttu-id="e376e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e376e-118">**String**</span></span> <br/> | <span data-ttu-id="e376e-119">Liste dans laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="e376e-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="e376e-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="e376e-120">_delimiter_</span></span> <br/> |<span data-ttu-id="e376e-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e376e-121">Optional</span></span>  <br/> |<span data-ttu-id="e376e-122">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e376e-122">**String**</span></span> <br/> | <span data-ttu-id="e376e-123">Chaîne à utiliser en tant que délimiteur dans la _liste_.</span><span class="sxs-lookup"><span data-stu-id="e376e-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="e376e-124">Une __ chaîne de délimiteur peut contenir plusieurs caractères et peut inclure des caractères multioctets.</span><span class="sxs-lookup"><span data-stu-id="e376e-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="e376e-125">La valeur par défaut est le point-virgule.</span><span class="sxs-lookup"><span data-stu-id="e376e-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e376e-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e376e-126">Return value</span></span>

<span data-ttu-id="e376e-127">Numérique</span><span class="sxs-lookup"><span data-stu-id="e376e-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e376e-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="e376e-128">Remarks</span></span>

<span data-ttu-id="e376e-p102">La fonction LOOKUP ne tient pas compte des majuscules ou des minuscules. Si la liste commence ou finit par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle.</span><span class="sxs-lookup"><span data-stu-id="e376e-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="e376e-p103">Tous les arguments doivent être des chaînes ou des expressions qui peuvent être convertis en chaînes. Si la conversion est impossible, une chaîne vide vient remplacer l’argument non accepté.</span><span class="sxs-lookup"><span data-stu-id="e376e-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e376e-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e376e-134">Example 1</span></span>

<span data-ttu-id="e376e-135">LOOKUP ("rat", "cat; rat;; chèvre ")</span><span class="sxs-lookup"><span data-stu-id="e376e-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="e376e-136">Renvoie 1.</span><span class="sxs-lookup"><span data-stu-id="e376e-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e376e-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e376e-137">Example 2</span></span>

<span data-ttu-id="e376e-138">LOOKUP ("", "; cat; rat;; chèvre ")</span><span class="sxs-lookup"><span data-stu-id="e376e-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="e376e-139">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="e376e-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e376e-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e376e-140">Example 3</span></span>

<span data-ttu-id="e376e-141">LOOKUP ("t", "cat; rat;; chèvre "," a ")</span><span class="sxs-lookup"><span data-stu-id="e376e-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="e376e-142">Renvoie 3.</span><span class="sxs-lookup"><span data-stu-id="e376e-142">Returns 3.</span></span>
  

