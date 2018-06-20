---
title: SETATREFEVAL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Utilisé dans le paramètre set_expression de la fonction SETATREF pour indiquer que set_expression devrait être évalué avant d’affecter au paramètre reference dans SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789612"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="ed131-103">SETATREFEVAL, fonction</span><span class="sxs-lookup"><span data-stu-id="ed131-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="ed131-104">Utilisé dans le paramètre _set_expression_ de la fonction SETATREF pour indiquer que _set_expression_ devrait être évalué avant d’affecter au paramètre _reference_ dans SETATREF.</span><span class="sxs-lookup"><span data-stu-id="ed131-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed131-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed131-105">Syntax</span></span>

<span data-ttu-id="ed131-106">SETATREFEVAL (** *expr* **)</span><span class="sxs-lookup"><span data-stu-id="ed131-106">SETATREFEVAL(** *expr* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed131-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed131-107">Parameters</span></span>

|<span data-ttu-id="ed131-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ed131-108">**Name**</span></span>|<span data-ttu-id="ed131-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ed131-109">**Required/Optional**</span></span>|<span data-ttu-id="ed131-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ed131-110">**Data Type**</span></span>|<span data-ttu-id="ed131-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ed131-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed131-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="ed131-112">_expr_</span></span> <br/> |<span data-ttu-id="ed131-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ed131-113">Required</span></span>  <br/> |<span data-ttu-id="ed131-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="ed131-114">**Varies**</span></span> <br/> | <span data-ttu-id="ed131-115">Une expression qui est évaluée lorsque la fonction SETATREF redirige _set_expression_ vers une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="ed131-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed131-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed131-116">Remarks</span></span>

<span data-ttu-id="ed131-117">Lorsque vous affectez le paramètre *set_expression* de la fonction SETATREF à une cellule référencée, Microsoft Visio écrit *set_expression* à la cellule comme une expression par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed131-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="ed131-118">Toutefois, si n’importe quelle partie du paramètre *set_expression* est encapsulée par la fonction SETATREFEVAL, Visio évalue l’expression et remplace la fonction SETATREFEVAL par son résultat avant de résoudre l’expression SETATREF.</span><span class="sxs-lookup"><span data-stu-id="ed131-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ed131-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed131-119">Example</span></span>

<span data-ttu-id="ed131-120">Pour obtenir un exemple, reportez-vous à la fonction [SETATREF](setatref-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ed131-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

