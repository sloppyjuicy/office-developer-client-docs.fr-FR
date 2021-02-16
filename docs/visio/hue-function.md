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
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439491"
---
# <a name="hue-function"></a><span data-ttu-id="de393-103">Fonction HUE</span><span class="sxs-lookup"><span data-stu-id="de393-103">HUE Function</span></span>

<span data-ttu-id="de393-104">Renvoie la valeur du composant de teinte d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="de393-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="de393-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de393-105">Syntax</span></span>

<span data-ttu-id="de393-106">HUE(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="de393-106">HUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="de393-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de393-107">Parameters</span></span>

|<span data-ttu-id="de393-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="de393-108">**Name**</span></span>|<span data-ttu-id="de393-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="de393-109">**Required/Optional**</span></span>|<span data-ttu-id="de393-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="de393-110">**Data Type**</span></span>|<span data-ttu-id="de393-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="de393-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="de393-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="de393-112">_expression_</span></span> <br/> |<span data-ttu-id="de393-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="de393-113">Required</span></span>  <br/> |<span data-ttu-id="de393-114">**String**</span><span class="sxs-lookup"><span data-stu-id="de393-114">**String**</span></span> <br/> |<span data-ttu-id="de393-115">Expression qui renvoie à une couleur.</span><span class="sxs-lookup"><span data-stu-id="de393-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="de393-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="de393-116">Return value</span></span>

<span data-ttu-id="de393-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="de393-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de393-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="de393-118">Remarks</span></span>

<span data-ttu-id="de393-p101">La valeur renvoyée est un nombre compris entre 0 et 239 inclus. L’entrée est l’index d’une couleur de la table du document, une expression qui produit une couleur personnalisée (telle que RVB ou TSL) ou une référence à une cellule contenant un index ou un résultat de couleurs. La fonction renvoie 0 si l’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="de393-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="de393-122">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="de393-122">Example 1</span></span>

<span data-ttu-id="de393-123">HUE(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="de393-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="de393-124">Renvoie la composante teinte de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="de393-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="de393-125">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="de393-125">Example 2</span></span>

<span data-ttu-id="de393-126">HUE(7)</span><span class="sxs-lookup"><span data-stu-id="de393-126">HUE(7)</span></span>
  
<span data-ttu-id="de393-127">Renvoie 120 si le document utilise la palette de couleurs par défaut de Microsoft Visio, où cyan est la couleur figurant à l’index 7.</span><span class="sxs-lookup"><span data-stu-id="de393-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="de393-128">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="de393-128">Example 3</span></span>

<span data-ttu-id="de393-129">HUE(HSL(10, 20, 30) )</span><span class="sxs-lookup"><span data-stu-id="de393-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="de393-130">Renvoie 10.</span><span class="sxs-lookup"><span data-stu-id="de393-130">Returns 10.</span></span>
  

