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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341138"
---
# <a name="not-function"></a><span data-ttu-id="474d9-104">Fonction NOT</span><span class="sxs-lookup"><span data-stu-id="474d9-104">NOT Function</span></span>

<span data-ttu-id="474d9-105">Renvoie la valeur TRUE (1) si _l'expression logicalexpression_ a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="474d9-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="474d9-106">Dans le cas contraire, elle renvoie la valeur FALSe (0).</span><span class="sxs-lookup"><span data-stu-id="474d9-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="474d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="474d9-107">Syntax</span></span>

<span data-ttu-id="474d9-108">NOT (\* \* *l'expression logicalexpression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="474d9-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="474d9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="474d9-109">Parameters</span></span>

|<span data-ttu-id="474d9-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="474d9-110">**Name**</span></span>|<span data-ttu-id="474d9-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="474d9-111">**Required/Optional**</span></span>|<span data-ttu-id="474d9-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="474d9-112">**Data Type**</span></span>|<span data-ttu-id="474d9-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="474d9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="474d9-114">_l'expression logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="474d9-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="474d9-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="474d9-115">Required</span></span>  <br/> |<span data-ttu-id="474d9-116">**String**</span><span class="sxs-lookup"><span data-stu-id="474d9-116">**String**</span></span> <br/> |<span data-ttu-id="474d9-117">Expression logique à évaluer</span><span class="sxs-lookup"><span data-stu-id="474d9-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="474d9-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="474d9-118">Return value</span></span>

<span data-ttu-id="474d9-119">Booléen</span><span class="sxs-lookup"><span data-stu-id="474d9-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="474d9-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="474d9-120">Example</span></span>

<span data-ttu-id="474d9-121">NOT (hauteur \> 0,75)</span><span class="sxs-lookup"><span data-stu-id="474d9-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="474d9-122">Renvoie 1 si la valeur de Hauteur est inférieure ou égale à 19,1 mm.</span><span class="sxs-lookup"><span data-stu-id="474d9-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="474d9-123">Renvoie 0 si la valeur de Hauteur est supérieure à 19,1 mm.</span><span class="sxs-lookup"><span data-stu-id="474d9-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

