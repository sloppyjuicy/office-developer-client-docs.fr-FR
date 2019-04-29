---
title: NOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Renvoie la valeur TRUE (1) si l'expression logicalexpression a la valeur FALSe. Dans le cas contraire, elle renvoie la valeur FALSe (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413331"
---
# <a name="not-function"></a><span data-ttu-id="adacb-104">Fonction NOT</span><span class="sxs-lookup"><span data-stu-id="adacb-104">NOT Function</span></span>

<span data-ttu-id="adacb-105">Renvoie la valeur TRUE (1) si _l'expression logicalexpression_ a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="adacb-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="adacb-106">Dans le cas contraire, elle renvoie la valeur FALSe (0).</span><span class="sxs-lookup"><span data-stu-id="adacb-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="adacb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adacb-107">Syntax</span></span>

<span data-ttu-id="adacb-108">NOT (\* \* *l'expression logicalexpression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="adacb-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="adacb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adacb-109">Parameters</span></span>

|<span data-ttu-id="adacb-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="adacb-110">**Name**</span></span>|<span data-ttu-id="adacb-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="adacb-111">**Required/Optional**</span></span>|<span data-ttu-id="adacb-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="adacb-112">**Data Type**</span></span>|<span data-ttu-id="adacb-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="adacb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="adacb-114">_l'expression logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="adacb-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="adacb-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="adacb-115">Required</span></span>  <br/> |<span data-ttu-id="adacb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="adacb-116">**String**</span></span> <br/> |<span data-ttu-id="adacb-117">Expression logique à évaluer</span><span class="sxs-lookup"><span data-stu-id="adacb-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="adacb-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="adacb-118">Return value</span></span>

<span data-ttu-id="adacb-119">Booléen</span><span class="sxs-lookup"><span data-stu-id="adacb-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="adacb-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="adacb-120">Example</span></span>

<span data-ttu-id="adacb-121">NOT (hauteur \> 0,75)</span><span class="sxs-lookup"><span data-stu-id="adacb-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="adacb-122">Renvoie 1 si la valeur de Hauteur est inférieure ou égale à 19,1 mm.</span><span class="sxs-lookup"><span data-stu-id="adacb-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="adacb-123">Renvoie 0 si la valeur de Hauteur est supérieure à 19,1 mm.</span><span class="sxs-lookup"><span data-stu-id="adacb-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

