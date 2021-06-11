---
title: LUM, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Renvoie la valeur du composant de luminosité d’une couleur.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419337"
---
# <a name="lum-function"></a><span data-ttu-id="9ad28-103">Fonction LUM</span><span class="sxs-lookup"><span data-stu-id="9ad28-103">LUM Function</span></span>

<span data-ttu-id="9ad28-104">Renvoie la valeur du composant de luminosité d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="9ad28-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9ad28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ad28-105">Syntax</span></span>

<span data-ttu-id="9ad28-106">LUM(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="9ad28-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9ad28-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ad28-107">Parameters</span></span>

|<span data-ttu-id="9ad28-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9ad28-108">**Name**</span></span>|<span data-ttu-id="9ad28-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9ad28-109">**Required/Optional**</span></span>|<span data-ttu-id="9ad28-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9ad28-110">**Data Type**</span></span>|<span data-ttu-id="9ad28-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9ad28-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9ad28-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="9ad28-112">_expression_</span></span> <br/> |<span data-ttu-id="9ad28-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ad28-113">Required</span></span>  <br/> |<span data-ttu-id="9ad28-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="9ad28-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9ad28-115">Index d’une couleur de la table des couleurs du document ou référence à une cellule qui contient un index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="9ad28-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9ad28-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ad28-116">Return value</span></span>

<span data-ttu-id="9ad28-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ad28-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ad28-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ad28-118">Remarks</span></span>

<span data-ttu-id="9ad28-p101">La valeur renvoyée est un nombre compris entre 0 et 240 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ad28-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9ad28-121">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="9ad28-121">Example 1</span></span>

<span data-ttu-id="9ad28-122">LUM(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="9ad28-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="9ad28-123">Renvoie la composante luminosité de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="9ad28-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9ad28-124">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="9ad28-124">Example 2</span></span>

<span data-ttu-id="9ad28-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="9ad28-125">LUM(6)</span></span>
  
<span data-ttu-id="9ad28-126">Renvoie 120 si le document utilise la palette de couleurs par défaut de Visio où magenta est la couleur correspondant à l’index 6.</span><span class="sxs-lookup"><span data-stu-id="9ad28-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9ad28-127">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="9ad28-127">Example 3</span></span>

<span data-ttu-id="9ad28-128">LUM(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="9ad28-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="9ad28-129">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="9ad28-129">Returns 30.</span></span>
  

