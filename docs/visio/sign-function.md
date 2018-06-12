---
title: SIGN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Renvoie une valeur qui représente le signe d’un nombre.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789747"
---
# <a name="sign-function"></a><span data-ttu-id="8aeb4-103">SIGN, fonction</span><span class="sxs-lookup"><span data-stu-id="8aeb4-103">SIGN Function</span></span>

<span data-ttu-id="8aeb4-104">Renvoie une valeur qui représente le signe d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8aeb4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8aeb4-105">Syntax</span></span>

<span data-ttu-id="8aeb4-106">CONNEXION (** *numéro* **, ** *robustesse* **)</span><span class="sxs-lookup"><span data-stu-id="8aeb4-106">SIGN(** *number* **, ** *fuzz* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8aeb4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8aeb4-107">Parameters</span></span>

|<span data-ttu-id="8aeb4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8aeb4-108">**Name**</span></span>|<span data-ttu-id="8aeb4-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8aeb4-109">**Required/Optional**</span></span>|<span data-ttu-id="8aeb4-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8aeb4-110">**Data Type**</span></span>|<span data-ttu-id="8aeb4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8aeb4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8aeb4-112">_number_</span><span class="sxs-lookup"><span data-stu-id="8aeb4-112">_number_</span></span> <br/> |<span data-ttu-id="8aeb4-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8aeb4-113">Required</span></span>  <br/> |<span data-ttu-id="8aeb4-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8aeb4-114">**Numeric**</span></span> <br/> | <span data-ttu-id="8aeb4-115">Nombre dont vous voulez déterminer le signe.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="8aeb4-116">_aléatoires_</span><span class="sxs-lookup"><span data-stu-id="8aeb4-116">_fuzz_</span></span> <br/> |<span data-ttu-id="8aeb4-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="8aeb4-117">Optional</span></span>  <br/> |<span data-ttu-id="8aeb4-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8aeb4-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8aeb4-119">Spécifie à partir de quelle valeur proche de zéro le nombre sera considéré comme égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8aeb4-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8aeb4-120">Return value</span></span>

<span data-ttu-id="8aeb4-121">Numérique</span><span class="sxs-lookup"><span data-stu-id="8aeb4-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8aeb4-122">Note</span><span class="sxs-lookup"><span data-stu-id="8aeb4-122">Remarks</span></span>

<span data-ttu-id="8aeb4-123">La fonction SIGN renvoie 1 si le _nombre_ est positif, 0 si le _nombre_ est égal à zéro ou -1 si le _nombre_ est négatif.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="8aeb4-124">Specifyin une valeur _aléatoire_ permet d’éviter les erreurs de l’argument à virgule flottante lorsqu’un calcul est presque égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="8aeb4-125">Si vous ne spécifiez pas une valeur _robustesse_ , Visio utilise 1E-9 (0,000000001).</span><span class="sxs-lookup"><span data-stu-id="8aeb4-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="8aeb4-126">Vous souhaiterez peut-être fournir une valeur différente lorsque vous redimensionnez dessins ou lorsque vous souhaitez une comparaison exacte.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8aeb4-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="8aeb4-127">Example 1</span></span>

<span data-ttu-id="8aeb4-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="8aeb4-128">SIGN(-5)</span></span>
  
<span data-ttu-id="8aeb4-129">Renvoie -1.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8aeb4-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="8aeb4-130">Example 2</span></span>

<span data-ttu-id="8aeb4-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="8aeb4-131">SIGN(0)</span></span>
  
<span data-ttu-id="8aeb4-132">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8aeb4-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="8aeb4-133">Example 3</span></span>

<span data-ttu-id="8aeb4-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="8aeb4-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="8aeb4-135">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="8aeb4-136">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="8aeb4-136">Example 4</span></span>

<span data-ttu-id="8aeb4-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="8aeb4-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="8aeb4-138">Renvoie 1.</span><span class="sxs-lookup"><span data-stu-id="8aeb4-138">Returns 1.</span></span>
  

