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
description: Renvoie une valeur qui représente le signe d'un nombre.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357455"
---
# <a name="sign-function"></a><span data-ttu-id="4865e-103">Fonction SIGN</span><span class="sxs-lookup"><span data-stu-id="4865e-103">SIGN Function</span></span>

<span data-ttu-id="4865e-104">Renvoie une valeur qui représente le signe d'un nombre.</span><span class="sxs-lookup"><span data-stu-id="4865e-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4865e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4865e-105">Syntax</span></span>

<span data-ttu-id="4865e-106">SIGNE (\* \* *nombre* \* \*, \* \* *Fuzz* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4865e-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4865e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4865e-107">Parameters</span></span>

|<span data-ttu-id="4865e-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4865e-108">**Name**</span></span>|<span data-ttu-id="4865e-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="4865e-109">**Required/Optional**</span></span>|<span data-ttu-id="4865e-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="4865e-110">**Data Type**</span></span>|<span data-ttu-id="4865e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="4865e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4865e-112">_number_</span><span class="sxs-lookup"><span data-stu-id="4865e-112">_number_</span></span> <br/> |<span data-ttu-id="4865e-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4865e-113">Required</span></span>  <br/> |<span data-ttu-id="4865e-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="4865e-114">**Numeric**</span></span> <br/> | <span data-ttu-id="4865e-115">Nombre dont vous voulez déterminer le signe.</span><span class="sxs-lookup"><span data-stu-id="4865e-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="4865e-116">_approximative_</span><span class="sxs-lookup"><span data-stu-id="4865e-116">_fuzz_</span></span> <br/> |<span data-ttu-id="4865e-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="4865e-117">Optional</span></span>  <br/> |<span data-ttu-id="4865e-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="4865e-118">**Numeric**</span></span> <br/> |<span data-ttu-id="4865e-119">Spécifie à partir de quelle valeur proche de zéro le nombre sera considéré comme égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4865e-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4865e-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4865e-120">Return value</span></span>

<span data-ttu-id="4865e-121">Numérique</span><span class="sxs-lookup"><span data-stu-id="4865e-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4865e-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="4865e-122">Remarks</span></span>

<span data-ttu-id="4865e-123">La fonction SIGN renvoie 1 si le _nombre_ est positif, 0 si le _nombre_ est égal à zéro ou-1 si le _nombre_ est négatif.</span><span class="sxs-lookup"><span data-stu-id="4865e-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="4865e-124">Spécification une valeur __ de robustesse permet d'éviter les erreurs de roundoff de virgule flottante lorsqu'un calcul est presque égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4865e-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="4865e-125">Si vous ne spécifiez pas de valeur de _Fuzz_ , Visio utilise 1e-9 (0,000000001).</span><span class="sxs-lookup"><span data-stu-id="4865e-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="4865e-126">Cette option vous permet de fournir une valeur différente lorsque vous mettez des dessins à l’échelle ou lorsque vous souhaitez faire une comparaison exacte.</span><span class="sxs-lookup"><span data-stu-id="4865e-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4865e-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="4865e-127">Example 1</span></span>

<span data-ttu-id="4865e-128">SIGN (-5)</span><span class="sxs-lookup"><span data-stu-id="4865e-128">SIGN(-5)</span></span>
  
<span data-ttu-id="4865e-129">Renvoie -1.</span><span class="sxs-lookup"><span data-stu-id="4865e-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4865e-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="4865e-130">Example 2</span></span>

<span data-ttu-id="4865e-131">SIGNE (0)</span><span class="sxs-lookup"><span data-stu-id="4865e-131">SIGN(0)</span></span>
  
<span data-ttu-id="4865e-132">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="4865e-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4865e-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="4865e-133">Example 3</span></span>

<span data-ttu-id="4865e-134">SIGN (0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="4865e-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="4865e-135">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="4865e-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="4865e-136">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="4865e-136">Example 4</span></span>

<span data-ttu-id="4865e-137">SIGN (0.00000000001, 0)</span><span class="sxs-lookup"><span data-stu-id="4865e-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="4865e-138">Renvoie 1.</span><span class="sxs-lookup"><span data-stu-id="4865e-138">Returns 1.</span></span>
  

