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
description: Renvoie la composante verte d'une couleur.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360206"
---
# <a name="green-function"></a><span data-ttu-id="052fb-103">Fonction GREEN</span><span class="sxs-lookup"><span data-stu-id="052fb-103">GREEN Function</span></span>

<span data-ttu-id="052fb-104">Renvoie la composante verte d'une couleur.</span><span class="sxs-lookup"><span data-stu-id="052fb-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="052fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="052fb-105">Syntax</span></span>

<span data-ttu-id="052fb-106">VERT (\* \* *expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="052fb-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="052fb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="052fb-107">Parameters</span></span>

|<span data-ttu-id="052fb-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="052fb-108">**Name**</span></span>|<span data-ttu-id="052fb-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="052fb-109">**Required/Optional**</span></span>|<span data-ttu-id="052fb-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="052fb-110">**Data Type**</span></span>|<span data-ttu-id="052fb-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="052fb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="052fb-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="052fb-112">_expression_</span></span> <br/> |<span data-ttu-id="052fb-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="052fb-113">Required</span></span>  <br/> |<span data-ttu-id="052fb-114">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="052fb-114">**Varies**</span></span> <br/> |<span data-ttu-id="052fb-115">Un index d'une couleur dans la table des couleurs du document, une expression qui correspond à une couleur personnalisée (telle que RVB ou TSL) ou une référence à une cellule contenant un index ou un résultat de couleur.</span><span class="sxs-lookup"><span data-stu-id="052fb-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="052fb-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="052fb-116">Return value</span></span>

<span data-ttu-id="052fb-117">Entier</span><span class="sxs-lookup"><span data-stu-id="052fb-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="052fb-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="052fb-118">Remarks</span></span>

<span data-ttu-id="052fb-119">La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index.</span><span class="sxs-lookup"><span data-stu-id="052fb-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="052fb-120">Si *expression* n'est pas valide, elle renvoie 0 (noir).</span><span class="sxs-lookup"><span data-stu-id="052fb-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="052fb-121">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="052fb-121">Example 1</span></span>

<span data-ttu-id="052fb-122">VERT (feuille. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="052fb-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="052fb-123">Renvoie la composante verte de la couleur de remplissage de premier plan de feuille. couleur.</span><span class="sxs-lookup"><span data-stu-id="052fb-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="052fb-124">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="052fb-124">Example 2</span></span>

<span data-ttu-id="052fb-125">VERT (11)</span><span class="sxs-lookup"><span data-stu-id="052fb-125">GREEN(11)</span></span>
  
<span data-ttu-id="052fb-126">Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où jaune foncé est la couleur de l'index 11.</span><span class="sxs-lookup"><span data-stu-id="052fb-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="052fb-127">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="052fb-127">Example 3</span></span>

<span data-ttu-id="052fb-128">VERT (RVB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="052fb-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="052fb-129">Renvoie 20.</span><span class="sxs-lookup"><span data-stu-id="052fb-129">Returns 20.</span></span>
  

