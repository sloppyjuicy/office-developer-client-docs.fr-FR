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
description: Renvoie un index de base zéro qui indique l’emplacement de la sous-chaîne clé dans une liste ou renvoie -1 si la chaîne cible contient le séparateur.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789046"
---
# <a name="lookup-function"></a><span data-ttu-id="d250f-103">LOOKUP, fonction</span><span class="sxs-lookup"><span data-stu-id="d250f-103">LOOKUP Function</span></span>

<span data-ttu-id="d250f-104">Renvoie un index de base zéro qui indique l’emplacement de la sous-chaîne _clé_ dans une _liste_ou renvoie -1 si la chaîne cible contient le _séparateur_.</span><span class="sxs-lookup"><span data-stu-id="d250f-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d250f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d250f-105">Syntax</span></span>

<span data-ttu-id="d250f-106">RECHERCHE (« ** *clé* ** », » ** *liste* ** « [, » ** *délimiteur* ** »])</span><span class="sxs-lookup"><span data-stu-id="d250f-106">LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d250f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d250f-107">Parameters</span></span>

|<span data-ttu-id="d250f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d250f-108">**Name**</span></span>|<span data-ttu-id="d250f-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d250f-109">**Required/Optional**</span></span>|<span data-ttu-id="d250f-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d250f-110">**Data Type**</span></span>|<span data-ttu-id="d250f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d250f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d250f-112">_clé_</span><span class="sxs-lookup"><span data-stu-id="d250f-112">_key_</span></span> <br/> |<span data-ttu-id="d250f-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d250f-113">Required</span></span>  <br/> |<span data-ttu-id="d250f-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d250f-114">**String**</span></span> <br/> |<span data-ttu-id="d250f-115">Chaîne à rechercher</span><span class="sxs-lookup"><span data-stu-id="d250f-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="d250f-116">_liste_</span><span class="sxs-lookup"><span data-stu-id="d250f-116">_list_</span></span> <br/> |<span data-ttu-id="d250f-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d250f-117">Required</span></span>  <br/> |<span data-ttu-id="d250f-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d250f-118">**String**</span></span> <br/> | <span data-ttu-id="d250f-119">Liste dans laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="d250f-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="d250f-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="d250f-120">_delimiter_</span></span> <br/> |<span data-ttu-id="d250f-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d250f-121">Optional</span></span>  <br/> |<span data-ttu-id="d250f-122">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d250f-122">**String**</span></span> <br/> | <span data-ttu-id="d250f-123">La chaîne à utiliser comme délimiteur dans la _liste_.</span><span class="sxs-lookup"><span data-stu-id="d250f-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="d250f-124">Une chaîne de _délimiteur_ peut être plusieurs caractères et peut inclure des caractères codés.</span><span class="sxs-lookup"><span data-stu-id="d250f-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="d250f-125">La valeur par défaut est un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="d250f-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d250f-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d250f-126">Return value</span></span>

<span data-ttu-id="d250f-127">Numérique</span><span class="sxs-lookup"><span data-stu-id="d250f-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d250f-128">Note</span><span class="sxs-lookup"><span data-stu-id="d250f-128">Remarks</span></span>

<span data-ttu-id="d250f-p102">La fonction LOOKUP ne tient pas compte des majuscules ou des minuscules. Si la liste commence ou finit par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle.</span><span class="sxs-lookup"><span data-stu-id="d250f-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="d250f-p103">Tous les arguments doivent être des chaînes ou des expressions qui peuvent être convertis en chaînes. Si la conversion est impossible, une chaîne vide vient remplacer l’argument non accepté.</span><span class="sxs-lookup"><span data-stu-id="d250f-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d250f-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="d250f-134">Example 1</span></span>

<span data-ttu-id="d250f-135">LOOKUP("rat","chat;rat;;chèvre")</span><span class="sxs-lookup"><span data-stu-id="d250f-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="d250f-136">Renvoie 1.</span><span class="sxs-lookup"><span data-stu-id="d250f-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d250f-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="d250f-137">Example 2</span></span>

<span data-ttu-id="d250f-138">LOOKUP("",";chat;rat;;chèvre")</span><span class="sxs-lookup"><span data-stu-id="d250f-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="d250f-139">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="d250f-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d250f-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="d250f-140">Example 3</span></span>

<span data-ttu-id="d250f-141">LOOKUP("t","chat;rat;;chèvre","a")</span><span class="sxs-lookup"><span data-stu-id="d250f-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="d250f-142">Renvoie 3.</span><span class="sxs-lookup"><span data-stu-id="d250f-142">Returns 3.</span></span>
  

