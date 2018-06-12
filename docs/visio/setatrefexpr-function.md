---
title: SETATREFEXPR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Stocke une valeur qui est définie par une action dans l’interface utilisateur (IU) ou Automation.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789634"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="7dbda-103">SETATREFEXPR, fonction</span><span class="sxs-lookup"><span data-stu-id="7dbda-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="7dbda-104">Stocke une valeur qui est définie par une action dans l’interface utilisateur (IU) ou Automation.</span><span class="sxs-lookup"><span data-stu-id="7dbda-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7dbda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dbda-105">Syntax</span></span>

<span data-ttu-id="7dbda-106">SETATREFEXPR ([** *expr_facult* **])</span><span class="sxs-lookup"><span data-stu-id="7dbda-106">SETATREFEXPR ([ ** *expr_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7dbda-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dbda-107">Parameters</span></span>

|<span data-ttu-id="7dbda-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7dbda-108">**Name**</span></span>|<span data-ttu-id="7dbda-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7dbda-109">**Required/Optional**</span></span>|<span data-ttu-id="7dbda-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7dbda-110">**Data Type**</span></span>|<span data-ttu-id="7dbda-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7dbda-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7dbda-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="7dbda-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="7dbda-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7dbda-113">Optional</span></span>  <br/> |<span data-ttu-id="7dbda-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="7dbda-114">**Varies**</span></span> <br/> |<span data-ttu-id="7dbda-115">Une expression est remplacée par la valeur ou l’expression affectée à la cellule référencée dans la fonction SETATREF.</span><span class="sxs-lookup"><span data-stu-id="7dbda-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="7dbda-116">Si ne pas indiqué, sa valeur initiale est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="7dbda-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dbda-117">Note</span><span class="sxs-lookup"><span data-stu-id="7dbda-117">Remarks</span></span>

<span data-ttu-id="7dbda-118">La valeur d’une expression SETATREFEXPR peut également être définie à partir d’une fonction SETATREF dans une autre cellule référençant la cellule qui contient l’expression SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="7dbda-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="7dbda-119">Vous n’êtes pas limité à l’aide de la fonction SETATREFEXPR en tant que paramètre à la fonction SETATREF.</span><span class="sxs-lookup"><span data-stu-id="7dbda-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7dbda-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="7dbda-120">Example 1</span></span>

<span data-ttu-id="7dbda-121">L’exemple suivant utilise la fonction SETATREFEXPR pour garantir qu’une forme est aussi large que son texte.</span><span class="sxs-lookup"><span data-stu-id="7dbda-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="7dbda-122">Width =MAX(TEXTWIDTH(Texte),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="7dbda-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7dbda-123">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="7dbda-123">Example 2</span></span>

<span data-ttu-id="7dbda-p102">L’exemple suivant indique comment utiliser la fonction SETATREFEXPR pour que vos formes s’alignent sur une grille personnalisée. Les formules SETATREFEXPR sont placées dans les cellules PinX et PinY, entraînant l’alignement de l’axe de la forme sur la grille définie dans User.GridX et User.GridY.</span><span class="sxs-lookup"><span data-stu-id="7dbda-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="7dbda-126">User.GridX =2 mm</span><span class="sxs-lookup"><span data-stu-id="7dbda-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="7dbda-127">User.GridY =2 mm</span><span class="sxs-lookup"><span data-stu-id="7dbda-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="7dbda-128">PinX = INT (SETATREFEXPR () /User.GridX +.5)\*User.GridX</span><span class="sxs-lookup"><span data-stu-id="7dbda-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="7dbda-129">PinY = INT (SETATREFEXPR () /User.GridY +.5)\*User.GridY</span><span class="sxs-lookup"><span data-stu-id="7dbda-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7dbda-130">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="7dbda-130">Example 3</span></span>

<span data-ttu-id="7dbda-131">Pour obtenir un exemple utilisant la fonction SETATREFEXPR avec la fonction SETATREF, reportez-vous à la fonction [SETATREF](setatref-function.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbda-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

