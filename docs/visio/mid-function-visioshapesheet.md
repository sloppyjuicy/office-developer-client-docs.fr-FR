---
title: Fonction MID (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, selon le nombre de caractères que vous spécifiez.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789149"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="a6402-103">Fonction MID (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a6402-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a6402-104">Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, selon le nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="a6402-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a6402-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6402-105">Syntax</span></span>

<span data-ttu-id="a6402-106">MID (** *texte* **, ** *start_num* **, ** *nb_cars* **)</span><span class="sxs-lookup"><span data-stu-id="a6402-106">MID (** *text* **, ** *start_num* **, ** *num_chars* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a6402-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6402-107">Parameters</span></span>

|<span data-ttu-id="a6402-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a6402-108">**Name**</span></span>|<span data-ttu-id="a6402-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a6402-109">**Required/Optional**</span></span>|<span data-ttu-id="a6402-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a6402-110">**Data Type**</span></span>|<span data-ttu-id="a6402-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a6402-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a6402-112">_text_</span><span class="sxs-lookup"><span data-stu-id="a6402-112">_text_</span></span> <br/> |<span data-ttu-id="a6402-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a6402-113">Required</span></span>  <br/> |<span data-ttu-id="a6402-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6402-114">**String**</span></span> <br/> |<span data-ttu-id="a6402-115">Chaîne de texte qui contient les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="a6402-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="a6402-116">_Start_num_</span><span class="sxs-lookup"><span data-stu-id="a6402-116">_start_num_</span></span> <br/> |<span data-ttu-id="a6402-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a6402-117">Required</span></span>  <br/> |<span data-ttu-id="a6402-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="a6402-118">**Number**</span></span> <br/> |<span data-ttu-id="a6402-p101">Position du premier caractère à extraire. Le premier caractère de la chaîne de texte est à la position 1.</span><span class="sxs-lookup"><span data-stu-id="a6402-p101">The position of the first character you want to extract. The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="a6402-121">_nb_cars_</span><span class="sxs-lookup"><span data-stu-id="a6402-121">_num_chars_</span></span> <br/> |<span data-ttu-id="a6402-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a6402-122">Required</span></span>  <br/> |<span data-ttu-id="a6402-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="a6402-123">**Number**</span></span> <br/> |<span data-ttu-id="a6402-124">Nombre de caractères à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="a6402-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a6402-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a6402-125">Return value</span></span>

<span data-ttu-id="a6402-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="a6402-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6402-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6402-127">Remarks</span></span>

<span data-ttu-id="a6402-128">Si *start_num* est :</span><span class="sxs-lookup"><span data-stu-id="a6402-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="a6402-129">Supérieur à la longueur de *texte* , MID renvoie « » (texte vide).</span><span class="sxs-lookup"><span data-stu-id="a6402-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="a6402-130">Inférieur à la longueur du *texte* , mais *start_num* plus *num_chars* dépasse la longueur du *texte* , MID renvoie les caractères jusqu'à la fin du *texte* .</span><span class="sxs-lookup"><span data-stu-id="a6402-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="a6402-p102">inférieur à 1, MID renvoie la valeur d’erreur #VALEUR!.</span><span class="sxs-lookup"><span data-stu-id="a6402-p102">Less than 1, MID returns the #VALUE! error value.</span></span> 
    
<span data-ttu-id="a6402-133">Si *nb_cars* est négatif, MID renvoie la #VALUE !</span><span class="sxs-lookup"><span data-stu-id="a6402-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="a6402-134">valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a6402-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a6402-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="a6402-135">Example</span></span>

<span data-ttu-id="a6402-136">MID ("SSN 999-99-9999";5;11)</span><span class="sxs-lookup"><span data-stu-id="a6402-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="a6402-137">Renvoie 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="a6402-137">Returns 999-99-9999.</span></span> 
  

