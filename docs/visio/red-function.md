---
title: RED, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Renvoie la composante rouge d'une couleur.
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415522"
---
# <a name="red-function"></a><span data-ttu-id="052a2-103">Fonction RED</span><span class="sxs-lookup"><span data-stu-id="052a2-103">RED Function</span></span>

<span data-ttu-id="052a2-104">Renvoie la composante rouge d'une couleur.</span><span class="sxs-lookup"><span data-stu-id="052a2-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="052a2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="052a2-105">Syntax</span></span>

<span data-ttu-id="052a2-106">ROUGE (\* \* *expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="052a2-106">RED(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="052a2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="052a2-107">Parameters</span></span>

|<span data-ttu-id="052a2-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="052a2-108">**Name**</span></span>|<span data-ttu-id="052a2-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="052a2-109">**Required/Optional**</span></span>|<span data-ttu-id="052a2-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="052a2-110">**Data Type**</span></span>|<span data-ttu-id="052a2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="052a2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="052a2-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="052a2-112">_expression_</span></span> <br/> |<span data-ttu-id="052a2-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="052a2-113">Required</span></span>  <br/> |<span data-ttu-id="052a2-114">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="052a2-114">**Varies**</span></span> <br/> |<span data-ttu-id="052a2-115">Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.</span><span class="sxs-lookup"><span data-stu-id="052a2-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="052a2-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="052a2-116">Return value</span></span>

<span data-ttu-id="052a2-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="052a2-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="052a2-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="052a2-118">Remarks</span></span>

<span data-ttu-id="052a2-119">La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index.</span><span class="sxs-lookup"><span data-stu-id="052a2-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="052a2-120">Si _expression_ n'est pas valide, cette fonction renvoie 0 (noir).</span><span class="sxs-lookup"><span data-stu-id="052a2-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="052a2-121">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="052a2-121">Example 1</span></span>

<span data-ttu-id="052a2-122">ROUGE (22)</span><span class="sxs-lookup"><span data-stu-id="052a2-122">RED(22)</span></span>
  
<span data-ttu-id="052a2-123">Renvoie 51 si le document utilise la palette de couleurs par défaut de Microsoft Office Visio, où le gris foncé a l’index de couleur 22.</span><span class="sxs-lookup"><span data-stu-id="052a2-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="052a2-124">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="052a2-124">Example 2</span></span>

<span data-ttu-id="052a2-125">ROUGE (Char. Color)</span><span class="sxs-lookup"><span data-stu-id="052a2-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="052a2-126">Renvoie la valeur de la composante rouge de la couleur de police actuelle.</span><span class="sxs-lookup"><span data-stu-id="052a2-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="052a2-127">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="052a2-127">Example 3</span></span>

<span data-ttu-id="052a2-128">RED(RVB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="052a2-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="052a2-129">Renvoie 10.</span><span class="sxs-lookup"><span data-stu-id="052a2-129">Returns 10.</span></span>
  

