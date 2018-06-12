---
title: IF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Renvoie la valeur valeursivrai si l’expression logicalexpression a la valeur TRUE. Sinon, elle renvoie ValeurSiFaux.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788810"
---
# <a name="if-function"></a><span data-ttu-id="28346-104">IF, fonction</span><span class="sxs-lookup"><span data-stu-id="28346-104">IF Function</span></span>

<span data-ttu-id="28346-105">Renvoie la _valeur valeursivrai_ si _l’expression logicalexpression_ a la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="28346-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="28346-106">Sinon, elle renvoie _ValeurSiFaux_.</span><span class="sxs-lookup"><span data-stu-id="28346-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="28346-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28346-107">Syntax</span></span>

<span data-ttu-id="28346-108">IF (** *logicalexpression* **, ** *renvoie ValeurSiVrai* **, ** *ValeurSiFaux* **)</span><span class="sxs-lookup"><span data-stu-id="28346-108">IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28346-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28346-109">Parameters</span></span>

|<span data-ttu-id="28346-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="28346-110">**Name**</span></span>|<span data-ttu-id="28346-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="28346-111">**Required/Optional**</span></span>|<span data-ttu-id="28346-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="28346-112">**Data Type**</span></span>|<span data-ttu-id="28346-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="28346-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28346-114">_expression logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="28346-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="28346-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28346-115">Required</span></span>  <br/> |<span data-ttu-id="28346-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="28346-116">**String**</span></span> <br/> |<span data-ttu-id="28346-117">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="28346-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="28346-118">_renvoie ValeurSiVrai_</span><span class="sxs-lookup"><span data-stu-id="28346-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="28346-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28346-119">Required</span></span>  <br/> |<span data-ttu-id="28346-120">**Varie**</span><span class="sxs-lookup"><span data-stu-id="28346-120">**Varies**</span></span> <br/> |<span data-ttu-id="28346-121">Valeur à renvoyer si _l’expression logicalexpression_ a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="28346-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="28346-122">_ValeurSiFaux_</span><span class="sxs-lookup"><span data-stu-id="28346-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="28346-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28346-123">Required</span></span>  <br/> |<span data-ttu-id="28346-124">**Varie**</span><span class="sxs-lookup"><span data-stu-id="28346-124">**Varies**</span></span> <br/> | <span data-ttu-id="28346-125">Valeur à renvoyer si _l’expression logicalexpression_ a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="28346-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="28346-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="28346-126">Return value</span></span>

<span data-ttu-id="28346-127">Variable</span><span class="sxs-lookup"><span data-stu-id="28346-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="28346-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="28346-128">Example</span></span>

<span data-ttu-id="28346-129">IF (hauteur \> 1,25 dans, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="28346-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="28346-p103">Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm. Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.</span><span class="sxs-lookup"><span data-stu-id="28346-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

