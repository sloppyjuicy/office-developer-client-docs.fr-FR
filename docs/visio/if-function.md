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
description: Renvoie valueiftrue si logicalexpression a la valeur TRUE. Sinon, elle renvoie valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405470"
---
# <a name="if-function"></a><span data-ttu-id="57cbe-104">Fonction IF</span><span class="sxs-lookup"><span data-stu-id="57cbe-104">IF Function</span></span>

<span data-ttu-id="57cbe-105">Renvoie  _valueiftrue si_  _logicalexpression_ a la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="57cbe-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="57cbe-106">Sinon, elle renvoie  _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="57cbe-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="57cbe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57cbe-107">Syntax</span></span>

<span data-ttu-id="57cbe-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span><span class="sxs-lookup"><span data-stu-id="57cbe-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="57cbe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57cbe-109">Parameters</span></span>

|<span data-ttu-id="57cbe-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="57cbe-110">**Name**</span></span>|<span data-ttu-id="57cbe-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="57cbe-111">**Required/Optional**</span></span>|<span data-ttu-id="57cbe-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="57cbe-112">**Data Type**</span></span>|<span data-ttu-id="57cbe-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="57cbe-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="57cbe-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="57cbe-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="57cbe-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="57cbe-115">Required</span></span>  <br/> |<span data-ttu-id="57cbe-116">**String**</span><span class="sxs-lookup"><span data-stu-id="57cbe-116">**String**</span></span> <br/> |<span data-ttu-id="57cbe-117">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="57cbe-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="57cbe-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="57cbe-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="57cbe-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="57cbe-119">Required</span></span>  <br/> |<span data-ttu-id="57cbe-120">**Varie**</span><span class="sxs-lookup"><span data-stu-id="57cbe-120">**Varies**</span></span> <br/> |<span data-ttu-id="57cbe-121">Valeur à renvoyer si  _logicalexpression_ est true.</span><span class="sxs-lookup"><span data-stu-id="57cbe-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="57cbe-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="57cbe-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="57cbe-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="57cbe-123">Required</span></span>  <br/> |<span data-ttu-id="57cbe-124">**Varie**</span><span class="sxs-lookup"><span data-stu-id="57cbe-124">**Varies**</span></span> <br/> | <span data-ttu-id="57cbe-125">Valeur à renvoyer si  _logicalexpression_ est false.</span><span class="sxs-lookup"><span data-stu-id="57cbe-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="57cbe-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57cbe-126">Return value</span></span>

<span data-ttu-id="57cbe-127">Variables</span><span class="sxs-lookup"><span data-stu-id="57cbe-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="57cbe-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="57cbe-128">Example</span></span>

<span data-ttu-id="57cbe-129">IF(Height \> 1.25 in,5,7)</span><span class="sxs-lookup"><span data-stu-id="57cbe-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="57cbe-p103">Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm. Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.</span><span class="sxs-lookup"><span data-stu-id="57cbe-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

