---
title: Fonction LEFT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Renvoie l’ou les caractères de la plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788932"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="839d6-103">Fonction LEFT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="839d6-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="839d6-104">Renvoie l’ou les caractères de la plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="839d6-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="839d6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="839d6-105">Syntax</span></span>

<span data-ttu-id="839d6-106">GAUCHE (** *texte* **, [, ** *nb_cars_opt* **])</span><span class="sxs-lookup"><span data-stu-id="839d6-106">LEFT(** *text* **, [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="839d6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="839d6-107">Parameters</span></span>

|<span data-ttu-id="839d6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="839d6-108">**Name**</span></span>|<span data-ttu-id="839d6-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="839d6-109">**Required/Optional**</span></span>|<span data-ttu-id="839d6-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="839d6-110">**Data Type**</span></span>|<span data-ttu-id="839d6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="839d6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="839d6-112">_text_</span><span class="sxs-lookup"><span data-stu-id="839d6-112">_text_</span></span> <br/> |<span data-ttu-id="839d6-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="839d6-113">Required</span></span>  <br/> |<span data-ttu-id="839d6-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="839d6-114">**String**</span></span> <br/> |<span data-ttu-id="839d6-115">Chaîne de texte qui contient les caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="839d6-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="839d6-116">_nb_cars_opt_</span><span class="sxs-lookup"><span data-stu-id="839d6-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="839d6-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="839d6-117">Optional</span></span>  <br/> |<span data-ttu-id="839d6-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="839d6-118">**Numeric**</span></span> <br/> |<span data-ttu-id="839d6-119">Nombre de caractères à extraire.</span><span class="sxs-lookup"><span data-stu-id="839d6-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="839d6-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="839d6-120">Return value</span></span>

<span data-ttu-id="839d6-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="839d6-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="839d6-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="839d6-122">Remarks</span></span>

<span data-ttu-id="839d6-123">La valeur de _nb_cars_opt_ doit être supérieure ou égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="839d6-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="839d6-124">Si _nb_cars_opt_ est supérieur à la longueur du texte, gauche renvoie tout le texte.</span><span class="sxs-lookup"><span data-stu-id="839d6-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="839d6-125">Si _nb_cars_opt_ est omis, il est supposé pour être 1.</span><span class="sxs-lookup"><span data-stu-id="839d6-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="839d6-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="839d6-126">Example</span></span>

<span data-ttu-id="839d6-127">LEFT ("Janvier 1 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="839d6-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="839d6-128">Renvoie la valeur "Jan".</span><span class="sxs-lookup"><span data-stu-id="839d6-128">Returns the value "Jan".</span></span> 
  

