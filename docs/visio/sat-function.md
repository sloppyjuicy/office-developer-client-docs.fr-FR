---
title: SAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Renvoie la valeur du composant de saturation d’une couleur.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789591"
---
# <a name="sat-function"></a><span data-ttu-id="c0bc7-103">SAT, fonction</span><span class="sxs-lookup"><span data-stu-id="c0bc7-103">SAT Function</span></span>

<span data-ttu-id="c0bc7-104">Renvoie la valeur du composant de saturation d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="c0bc7-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c0bc7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0bc7-105">Syntax</span></span>

<span data-ttu-id="c0bc7-106">SAM (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="c0bc7-106">SAT(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0bc7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0bc7-107">Parameters</span></span>

|<span data-ttu-id="c0bc7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0bc7-108">**Name**</span></span>|<span data-ttu-id="c0bc7-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c0bc7-109">**Required/Optional**</span></span>|<span data-ttu-id="c0bc7-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c0bc7-110">**Data Type**</span></span>|<span data-ttu-id="c0bc7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0bc7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0bc7-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="c0bc7-112">_expression_</span></span> <br/> |<span data-ttu-id="c0bc7-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0bc7-113">Required</span></span>  <br/> |<span data-ttu-id="c0bc7-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="c0bc7-114">**Varies**</span></span> <br/> |<span data-ttu-id="c0bc7-115">Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.</span><span class="sxs-lookup"><span data-stu-id="c0bc7-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0bc7-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c0bc7-116">Return value</span></span>

<span data-ttu-id="c0bc7-117">Numérique</span><span class="sxs-lookup"><span data-stu-id="c0bc7-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0bc7-118">Note</span><span class="sxs-lookup"><span data-stu-id="c0bc7-118">Remarks</span></span>

<span data-ttu-id="c0bc7-p101">La valeur renvoyée est un nombre compris entre 0 et 240 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c0bc7-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="c0bc7-121">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="c0bc7-121">Example 1</span></span>

<span data-ttu-id="c0bc7-122">SAT (feuille.4 ! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="c0bc7-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="c0bc7-123">Renvoie la composante Saturation de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="c0bc7-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c0bc7-124">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="c0bc7-124">Example 2</span></span>

<span data-ttu-id="c0bc7-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="c0bc7-125">SAT(8)</span></span>
  
<span data-ttu-id="c0bc7-126">Renvoie 240 si le document utilise la palette de couleurs par défaut de Visio où rouge foncé est la couleur de l’index 8.</span><span class="sxs-lookup"><span data-stu-id="c0bc7-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c0bc7-127">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="c0bc7-127">Example 3</span></span>

<span data-ttu-id="c0bc7-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="c0bc7-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="c0bc7-129">Renvoie 20.</span><span class="sxs-lookup"><span data-stu-id="c0bc7-129">Returns 20.</span></span>
  

