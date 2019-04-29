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
description: Utilisé dans le paramètre Set_Expression de la fonction SETATREF pour indiquer que Set_Expression doit être évalué avant d'être affecté au paramètre Reference dans SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432981"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="4c983-103">Fonction SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="4c983-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="4c983-104">Utilisé dans le paramètre _set_expression_ de la fonction SETATREF pour indiquer que _set_expression_ doit être évalué avant d'être affecté au paramètre _Reference_ dans SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4c983-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4c983-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c983-105">Syntax</span></span>

<span data-ttu-id="4c983-106">SETATREFEVAL (\* \* *expr* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4c983-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4c983-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c983-107">Parameters</span></span>

|<span data-ttu-id="4c983-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4c983-108">**Name**</span></span>|<span data-ttu-id="4c983-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="4c983-109">**Required/Optional**</span></span>|<span data-ttu-id="4c983-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="4c983-110">**Data Type**</span></span>|<span data-ttu-id="4c983-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c983-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4c983-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="4c983-112">_expr_</span></span> <br/> |<span data-ttu-id="4c983-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c983-113">Required</span></span>  <br/> |<span data-ttu-id="4c983-114">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="4c983-114">**Varies**</span></span> <br/> | <span data-ttu-id="4c983-115">Expression évaluée lorsque la fonction SETATREF redirige _set_expression_ vers une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="4c983-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c983-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c983-116">Remarks</span></span>

<span data-ttu-id="4c983-117">Lors de l'assignation du paramètre *set_expression* de la fonction SETATREF à une cellule référencée, Microsoft Visio écrit *set_expression* dans la cellule en tant qu'expression par défaut.</span><span class="sxs-lookup"><span data-stu-id="4c983-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="4c983-118">Toutefois, si une partie du paramètre *set_expression* est encapsulée par la fonction SETATREFEVAL, Visio évalue l'expression et remplace la fonction SETATREFEVAL par son résultat avant de résoudre l'expression SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4c983-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4c983-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c983-119">Example</span></span>

<span data-ttu-id="4c983-120">Pour un exemple, reportez-vous à la fonction [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="4c983-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

