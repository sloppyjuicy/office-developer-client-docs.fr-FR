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
description: Renvoie le composant bleu d’une couleur. La valeur de retour est un nombre complet compris entre 0 et 255 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439036"
---
# <a name="blue-function"></a><span data-ttu-id="dacce-105">Fonction BLUE</span><span class="sxs-lookup"><span data-stu-id="dacce-105">BLUE Function</span></span>

<span data-ttu-id="dacce-106">Renvoie le composant bleu d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="dacce-106">Returns the blue component of a color.</span></span> <span data-ttu-id="dacce-107">La valeur de retour est un nombre complet compris entre 0 et 255 inclus.</span><span class="sxs-lookup"><span data-stu-id="dacce-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="dacce-108">La fonction renvoie 0 si l’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="dacce-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dacce-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dacce-109">Syntax</span></span>

<span data-ttu-id="dacce-110">BLUE(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="dacce-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dacce-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dacce-111">Parameters</span></span>

|<span data-ttu-id="dacce-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dacce-112">**Name**</span></span>|<span data-ttu-id="dacce-113">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="dacce-113">**Required/Optional**</span></span>|<span data-ttu-id="dacce-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="dacce-114">**Data Type**</span></span>|<span data-ttu-id="dacce-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="dacce-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dacce-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="dacce-116">_expression_</span></span> <br/> |<span data-ttu-id="dacce-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dacce-117">Required</span></span>  <br/> |<span data-ttu-id="dacce-118">**String**</span><span class="sxs-lookup"><span data-stu-id="dacce-118">**String**</span></span> <br/> |<span data-ttu-id="dacce-119">Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.</span><span class="sxs-lookup"><span data-stu-id="dacce-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dacce-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dacce-120">Return value</span></span>

<span data-ttu-id="dacce-121">Entier</span><span class="sxs-lookup"><span data-stu-id="dacce-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="dacce-122">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="dacce-122">Example 1</span></span>

<span data-ttu-id="dacce-123">BLUE(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="dacce-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="dacce-124">Renvoie la composante bleu de la couleur de remplissage de premier plan de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="dacce-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dacce-125">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="dacce-125">Example 2</span></span>

<span data-ttu-id="dacce-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="dacce-126">BLUE(13)</span></span>
  
<span data-ttu-id="dacce-127">Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où cyan est la couleur dont l’index est 13.</span><span class="sxs-lookup"><span data-stu-id="dacce-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dacce-128">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="dacce-128">Example 3</span></span>

<span data-ttu-id="dacce-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="dacce-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="dacce-130">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="dacce-130">Returns 30.</span></span>
  

