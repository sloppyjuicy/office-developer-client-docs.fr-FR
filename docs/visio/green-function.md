---
title: GREEN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Renvoie le composant vert d’une couleur.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438105"
---
# <a name="green-function"></a><span data-ttu-id="ab718-103">Fonction GREEN</span><span class="sxs-lookup"><span data-stu-id="ab718-103">GREEN Function</span></span>

<span data-ttu-id="ab718-104">Renvoie le composant vert d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="ab718-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ab718-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab718-105">Syntax</span></span>

<span data-ttu-id="ab718-106">GREEN(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ab718-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ab718-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab718-107">Parameters</span></span>

|<span data-ttu-id="ab718-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ab718-108">**Name**</span></span>|<span data-ttu-id="ab718-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ab718-109">**Required/Optional**</span></span>|<span data-ttu-id="ab718-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ab718-110">**Data Type**</span></span>|<span data-ttu-id="ab718-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab718-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ab718-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ab718-112">_expression_</span></span> <br/> |<span data-ttu-id="ab718-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ab718-113">Required</span></span>  <br/> |<span data-ttu-id="ab718-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="ab718-114">**Varies**</span></span> <br/> |<span data-ttu-id="ab718-115">Index d’une couleur dans le tableau des couleurs du document, expression qui se résout en une couleur personnalisée (par exemple, RVB ou HSL) ou une référence à une cellule qui contient un index de couleur ou un résultat de couleur.</span><span class="sxs-lookup"><span data-stu-id="ab718-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ab718-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab718-116">Return value</span></span>

<span data-ttu-id="ab718-117">Entier</span><span class="sxs-lookup"><span data-stu-id="ab718-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab718-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab718-118">Remarks</span></span>

<span data-ttu-id="ab718-119">La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index.</span><span class="sxs-lookup"><span data-stu-id="ab718-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="ab718-120">Si  *l’expression*  n’est pas valide, elle renvoie 0 (noir).</span><span class="sxs-lookup"><span data-stu-id="ab718-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ab718-121">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="ab718-121">Example 1</span></span>

<span data-ttu-id="ab718-122">GREEN(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="ab718-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ab718-123">Renvoie la composante verte de la couleur de premier plan de remplissage de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="ab718-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ab718-124">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="ab718-124">Example 2</span></span>

<span data-ttu-id="ab718-125">GREEN(11)</span><span class="sxs-lookup"><span data-stu-id="ab718-125">GREEN(11)</span></span>
  
<span data-ttu-id="ab718-126">Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où le jaune foncé est la couleur à l’index 11.</span><span class="sxs-lookup"><span data-stu-id="ab718-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ab718-127">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="ab718-127">Example 3</span></span>

<span data-ttu-id="ab718-128">GREEN(RVB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ab718-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="ab718-129">Renvoie 20.</span><span class="sxs-lookup"><span data-stu-id="ab718-129">Returns 20.</span></span>
  

