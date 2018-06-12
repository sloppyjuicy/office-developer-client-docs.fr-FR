---
title: HUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Renvoie la valeur du composant de teinte d’une couleur.
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788788"
---
# <a name="hue-function"></a><span data-ttu-id="e2a26-103">HUE, fonction</span><span class="sxs-lookup"><span data-stu-id="e2a26-103">HUE Function</span></span>

<span data-ttu-id="e2a26-104">Renvoie la valeur du composant de teinte d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="e2a26-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e2a26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2a26-105">Syntax</span></span>

<span data-ttu-id="e2a26-106">TEINTE (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="e2a26-106">HUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e2a26-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2a26-107">Parameters</span></span>

|<span data-ttu-id="e2a26-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e2a26-108">**Name**</span></span>|<span data-ttu-id="e2a26-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e2a26-109">**Required/Optional**</span></span>|<span data-ttu-id="e2a26-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e2a26-110">**Data Type**</span></span>|<span data-ttu-id="e2a26-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2a26-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e2a26-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="e2a26-112">_expression_</span></span> <br/> |<span data-ttu-id="e2a26-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2a26-113">Required</span></span>  <br/> |<span data-ttu-id="e2a26-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e2a26-114">**String**</span></span> <br/> |<span data-ttu-id="e2a26-115">Expression qui renvoie à une couleur.</span><span class="sxs-lookup"><span data-stu-id="e2a26-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e2a26-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e2a26-116">Return value</span></span>

<span data-ttu-id="e2a26-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="e2a26-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2a26-118">Note</span><span class="sxs-lookup"><span data-stu-id="e2a26-118">Remarks</span></span>

<span data-ttu-id="e2a26-p101">La valeur renvoyée est un nombre compris entre 0 et 239 inclus. L’entrée est l’index d’une couleur de la table du document, une expression qui produit une couleur personnalisée (telle que RVB ou TSL) ou une référence à une cellule contenant un index ou un résultat de couleurs. La fonction renvoie 0 si l’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e2a26-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e2a26-122">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e2a26-122">Example 1</span></span>

<span data-ttu-id="e2a26-123">TEINTE (feuille.4 ! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="e2a26-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="e2a26-124">Renvoie la composante teinte de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="e2a26-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e2a26-125">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e2a26-125">Example 2</span></span>

<span data-ttu-id="e2a26-126">HUE(7)</span><span class="sxs-lookup"><span data-stu-id="e2a26-126">HUE(7)</span></span>
  
<span data-ttu-id="e2a26-127">Renvoie 120 si le document utilise la palette de couleurs par défaut de Microsoft Visio, où cyan est la couleur figurant à l’index 7.</span><span class="sxs-lookup"><span data-stu-id="e2a26-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e2a26-128">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e2a26-128">Example 3</span></span>

<span data-ttu-id="e2a26-129">HUE(HSL(10, 20, 30) )</span><span class="sxs-lookup"><span data-stu-id="e2a26-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="e2a26-130">Renvoie 10.</span><span class="sxs-lookup"><span data-stu-id="e2a26-130">Returns 10.</span></span>
  

