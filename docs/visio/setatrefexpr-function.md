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
description: Stocke une valeur définie par le biais d’une action dans l’interface utilisateur (IU) ou Automation.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439050"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="1c058-103">Fonction SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="1c058-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="1c058-104">Stocke une valeur définie par le biais d’une action dans l’interface utilisateur (IU) ou Automation.</span><span class="sxs-lookup"><span data-stu-id="1c058-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1c058-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c058-105">Syntax</span></span>

<span data-ttu-id="1c058-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="1c058-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1c058-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c058-107">Parameters</span></span>

|<span data-ttu-id="1c058-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1c058-108">**Name**</span></span>|<span data-ttu-id="1c058-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1c058-109">**Required/Optional**</span></span>|<span data-ttu-id="1c058-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1c058-110">**Data Type**</span></span>|<span data-ttu-id="1c058-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c058-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1c058-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="1c058-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="1c058-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="1c058-113">Optional</span></span>  <br/> |<span data-ttu-id="1c058-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="1c058-114">**Varies**</span></span> <br/> |<span data-ttu-id="1c058-115">Expression remplacée par la valeur ou l’expression affectée à la cellule référencée dans la fonction SETATREF.</span><span class="sxs-lookup"><span data-stu-id="1c058-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="1c058-116">S’il n’est pas indiqué, sa valeur initiale est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="1c058-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c058-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c058-117">Remarks</span></span>

<span data-ttu-id="1c058-118">La valeur d’une expression SETATREFEXPR peut également être définie à partir d’une fonction SETATREF dans une autre cellule référençant la cellule qui contient l’expression SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="1c058-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="1c058-119">Vous n’êtes pas limité à l’utilisation de la fonction SETATREFEXPR comme paramètre de la fonction SETATREF.</span><span class="sxs-lookup"><span data-stu-id="1c058-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1c058-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="1c058-120">Example 1</span></span>

<span data-ttu-id="1c058-121">L’exemple suivant utilise la fonction SETATREFEXPR pour garantir qu’une forme est aussi large que son texte.</span><span class="sxs-lookup"><span data-stu-id="1c058-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="1c058-122">Width =MAX(TEXTWIDTH(Texte),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="1c058-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1c058-123">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="1c058-123">Example 2</span></span>

<span data-ttu-id="1c058-p102">L’exemple suivant indique comment utiliser la fonction SETATREFEXPR pour que vos formes s’alignent sur une grille personnalisée. Les formules SETATREFEXPR sont placées dans les cellules PinX et PinY, entraînant l’alignement de l’axe de la forme sur la grille définie dans User.GridX et User.GridY.</span><span class="sxs-lookup"><span data-stu-id="1c058-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="1c058-126">User.GridX =2 mm</span><span class="sxs-lookup"><span data-stu-id="1c058-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="1c058-127">User.GridY =2 mm</span><span class="sxs-lookup"><span data-stu-id="1c058-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="1c058-128">PinX =INT(SETATREFEXPR()/User.GridX + .5) \* User.GridX</span><span class="sxs-lookup"><span data-stu-id="1c058-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="1c058-129">PinY =INT(SETATREFEXPR()/User.GridY + .5) \* User.GridY</span><span class="sxs-lookup"><span data-stu-id="1c058-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1c058-130">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="1c058-130">Example 3</span></span>

<span data-ttu-id="1c058-131">Pour un exemple utilisant la fonction SETATREFEXPR avec la fonction SETATREF, reportez-vous à la fonction [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="1c058-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

