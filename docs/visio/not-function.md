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
description: Renvoie la valeur TRUE (1) si l’expression logicalexpression a la valeur FALSE. Dans le cas contraire, elle renvoie la valeur FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789173"
---
# <a name="not-function"></a><span data-ttu-id="09439-104">NOT, fonction</span><span class="sxs-lookup"><span data-stu-id="09439-104">NOT Function</span></span>

<span data-ttu-id="09439-105">Renvoie la valeur TRUE (1) si _l’expression logicalexpression_ a la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="09439-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="09439-106">Dans le cas contraire, elle renvoie la valeur FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="09439-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="09439-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09439-107">Syntax</span></span>

<span data-ttu-id="09439-108">NON (** *logicalexpression* **)</span><span class="sxs-lookup"><span data-stu-id="09439-108">NOT(** *logicalexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="09439-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09439-109">Parameters</span></span>

|<span data-ttu-id="09439-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="09439-110">**Name**</span></span>|<span data-ttu-id="09439-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="09439-111">**Required/Optional**</span></span>|<span data-ttu-id="09439-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="09439-112">**Data Type**</span></span>|<span data-ttu-id="09439-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="09439-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="09439-114">_expression logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="09439-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="09439-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="09439-115">Required</span></span>  <br/> |<span data-ttu-id="09439-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="09439-116">**String**</span></span> <br/> |<span data-ttu-id="09439-117">Expression logique à évaluer</span><span class="sxs-lookup"><span data-stu-id="09439-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="09439-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="09439-118">Return value</span></span>

<span data-ttu-id="09439-119">Booléenne</span><span class="sxs-lookup"><span data-stu-id="09439-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="09439-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="09439-120">Example</span></span>

<span data-ttu-id="09439-121">NON (hauteur \> in 0,75)</span><span class="sxs-lookup"><span data-stu-id="09439-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="09439-p103">Renvoie 1 si la valeur de Hauteur est inférieure ou égale à 19,1 mm. Renvoie 0 si la valeur de Hauteur est supérieure à 19,1 mm.</span><span class="sxs-lookup"><span data-stu-id="09439-p103">Returns 1 if Height is less than or equal to 0.75 inches. Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

