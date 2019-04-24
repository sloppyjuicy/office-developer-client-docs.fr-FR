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
description: Renvoie la composante bleu d'une couleur. La valeur renvoyée est un entier compris entre 0 et 255 (inclus). La fonction renvoie 0 si l’entrée n’est pas valide.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297353"
---
# <a name="blue-function"></a><span data-ttu-id="01596-105">Fonction BLUE</span><span class="sxs-lookup"><span data-stu-id="01596-105">BLUE Function</span></span>

<span data-ttu-id="01596-106">Renvoie la composante bleu d'une couleur.</span><span class="sxs-lookup"><span data-stu-id="01596-106">Returns the blue component of a color.</span></span> <span data-ttu-id="01596-107">La valeur renvoyée est un entier compris entre 0 et 255 (inclus).</span><span class="sxs-lookup"><span data-stu-id="01596-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="01596-108">La fonction renvoie 0 si l’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="01596-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="01596-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01596-109">Syntax</span></span>

<span data-ttu-id="01596-110">BLEU (\* \* *expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="01596-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="01596-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01596-111">Parameters</span></span>

|<span data-ttu-id="01596-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="01596-112">**Name**</span></span>|<span data-ttu-id="01596-113">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="01596-113">**Required/Optional**</span></span>|<span data-ttu-id="01596-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="01596-114">**Data Type**</span></span>|<span data-ttu-id="01596-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="01596-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="01596-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="01596-116">_expression_</span></span> <br/> |<span data-ttu-id="01596-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="01596-117">Required</span></span>  <br/> |<span data-ttu-id="01596-118">**String**</span><span class="sxs-lookup"><span data-stu-id="01596-118">**String**</span></span> <br/> |<span data-ttu-id="01596-119">Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.</span><span class="sxs-lookup"><span data-stu-id="01596-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="01596-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01596-120">Return value</span></span>

<span data-ttu-id="01596-121">Entier</span><span class="sxs-lookup"><span data-stu-id="01596-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="01596-122">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="01596-122">Example 1</span></span>

<span data-ttu-id="01596-123">BLEU (feuille. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="01596-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="01596-124">Renvoie la composante bleu de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="01596-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="01596-125">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="01596-125">Example 2</span></span>

<span data-ttu-id="01596-126">BLEU (13)</span><span class="sxs-lookup"><span data-stu-id="01596-126">BLUE(13)</span></span>
  
<span data-ttu-id="01596-127">Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où cyan est la couleur dont l’index est 13.</span><span class="sxs-lookup"><span data-stu-id="01596-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="01596-128">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="01596-128">Example 3</span></span>

<span data-ttu-id="01596-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="01596-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="01596-130">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="01596-130">Returns 30.</span></span>
  

