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
description: Renvoie valueiftrue si l'expression logicalexpression a la valeur TRUE. Dans le cas contraire, elle renvoie valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344764"
---
# <a name="if-function"></a><span data-ttu-id="2d9df-104">Fonction IF</span><span class="sxs-lookup"><span data-stu-id="2d9df-104">IF Function</span></span>

<span data-ttu-id="2d9df-105">Renvoie _valueiftrue_ si _l'expression LOGICALEXPRESSION_ a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="2d9df-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="2d9df-106">Dans le cas contraire, elle renvoie _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="2d9df-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2d9df-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d9df-107">Syntax</span></span>

<span data-ttu-id="2d9df-108">IF (\* \* *l'expression logicalexpression* \* \*, \* \* *valueiftrue* \* \*, \* \* *valueiffalse* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2d9df-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2d9df-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d9df-109">Parameters</span></span>

|<span data-ttu-id="2d9df-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2d9df-110">**Name**</span></span>|<span data-ttu-id="2d9df-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="2d9df-111">**Required/Optional**</span></span>|<span data-ttu-id="2d9df-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2d9df-112">**Data Type**</span></span>|<span data-ttu-id="2d9df-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="2d9df-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2d9df-114">_l'expression logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="2d9df-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="2d9df-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d9df-115">Required</span></span>  <br/> |<span data-ttu-id="2d9df-116">**String**</span><span class="sxs-lookup"><span data-stu-id="2d9df-116">**String**</span></span> <br/> |<span data-ttu-id="2d9df-117">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="2d9df-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2d9df-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="2d9df-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="2d9df-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d9df-119">Required</span></span>  <br/> |<span data-ttu-id="2d9df-120">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="2d9df-120">**Varies**</span></span> <br/> |<span data-ttu-id="2d9df-121">Valeur à renvoyer si _l'expression logicalexpression_ a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="2d9df-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="2d9df-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="2d9df-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="2d9df-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d9df-123">Required</span></span>  <br/> |<span data-ttu-id="2d9df-124">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="2d9df-124">**Varies**</span></span> <br/> | <span data-ttu-id="2d9df-125">Valeur à renvoyer si _l'expression logicalexpression_ est false.</span><span class="sxs-lookup"><span data-stu-id="2d9df-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2d9df-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d9df-126">Return value</span></span>

<span data-ttu-id="2d9df-127">Variables</span><span class="sxs-lookup"><span data-stu-id="2d9df-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="2d9df-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="2d9df-128">Example</span></span>

<span data-ttu-id="2d9df-129">Si (hauteur \> 1,25, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="2d9df-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="2d9df-130">Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm.</span><span class="sxs-lookup"><span data-stu-id="2d9df-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="2d9df-131">Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.</span><span class="sxs-lookup"><span data-stu-id="2d9df-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

