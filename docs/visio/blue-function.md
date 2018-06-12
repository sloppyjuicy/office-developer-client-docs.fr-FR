---
title: BLUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Renvoie la composante bleu d’une couleur. La valeur de retour est un entier compris entre 0 et 255, inclus. La fonction renvoie la valeur 0 pour une entrée non valide.
ms.openlocfilehash: 6a86a0ee91054c89f2def95c0e3521508462bdaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788153"
---
# <a name="blue-function"></a><span data-ttu-id="2e833-105">BLUE, fonction</span><span class="sxs-lookup"><span data-stu-id="2e833-105">BLUE Function</span></span>

<span data-ttu-id="2e833-106">Renvoie la composante bleu d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="2e833-106">Returns the blue component of a color.</span></span> <span data-ttu-id="2e833-107">La valeur de retour est un entier compris entre 0 et 255, inclus.</span><span class="sxs-lookup"><span data-stu-id="2e833-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="2e833-108">La fonction renvoie la valeur 0 pour une entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="2e833-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2e833-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e833-109">Syntax</span></span>

<span data-ttu-id="2e833-110">BLEU (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="2e833-110">BLUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e833-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e833-111">Parameters</span></span>

|<span data-ttu-id="2e833-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e833-112">**Name**</span></span>|<span data-ttu-id="2e833-113">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="2e833-113">**Required/Optional**</span></span>|<span data-ttu-id="2e833-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2e833-114">**Data Type**</span></span>|<span data-ttu-id="2e833-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e833-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e833-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="2e833-116">_expression_</span></span> <br/> |<span data-ttu-id="2e833-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2e833-117">Required</span></span>  <br/> |<span data-ttu-id="2e833-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e833-118">**String**</span></span> <br/> |<span data-ttu-id="2e833-119">Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.</span><span class="sxs-lookup"><span data-stu-id="2e833-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2e833-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2e833-120">Return value</span></span>

<span data-ttu-id="2e833-121">Entier</span><span class="sxs-lookup"><span data-stu-id="2e833-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="2e833-122">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="2e833-122">Example 1</span></span>

<span data-ttu-id="2e833-123">BLEU (feuille.4 ! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="2e833-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="2e833-124">Renvoie la composante bleu de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="2e833-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2e833-125">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="2e833-125">Example 2</span></span>

<span data-ttu-id="2e833-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="2e833-126">BLUE(13)</span></span>
  
<span data-ttu-id="2e833-127">Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où cyan est la couleur dont l’index est 13.</span><span class="sxs-lookup"><span data-stu-id="2e833-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2e833-128">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="2e833-128">Example 3</span></span>

<span data-ttu-id="2e833-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="2e833-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="2e833-130">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="2e833-130">Returns 30.</span></span>
  

