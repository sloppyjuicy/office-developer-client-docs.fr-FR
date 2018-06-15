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
description: Renvoie la composante rouge d’une couleur.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789392"
---
# <a name="red-function"></a><span data-ttu-id="b8e16-103">RED, fonction</span><span class="sxs-lookup"><span data-stu-id="b8e16-103">RED Function</span></span>

<span data-ttu-id="b8e16-104">Renvoie la composante rouge d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="b8e16-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b8e16-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8e16-105">Syntax</span></span>

<span data-ttu-id="b8e16-106">ROUGE (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="b8e16-106">RED(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b8e16-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8e16-107">Parameters</span></span>

|<span data-ttu-id="b8e16-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8e16-108">**Name**</span></span>|<span data-ttu-id="b8e16-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b8e16-109">**Required/Optional**</span></span>|<span data-ttu-id="b8e16-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b8e16-110">**Data Type**</span></span>|<span data-ttu-id="b8e16-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8e16-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b8e16-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b8e16-112">_expression_</span></span> <br/> |<span data-ttu-id="b8e16-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b8e16-113">Required</span></span>  <br/> |<span data-ttu-id="b8e16-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="b8e16-114">**Varies**</span></span> <br/> |<span data-ttu-id="b8e16-115">Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.</span><span class="sxs-lookup"><span data-stu-id="b8e16-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b8e16-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b8e16-116">Return value</span></span>

<span data-ttu-id="b8e16-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="b8e16-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8e16-118">Note</span><span class="sxs-lookup"><span data-stu-id="b8e16-118">Remarks</span></span>

<span data-ttu-id="b8e16-119">La valeur de retour est un nombre compris entre 0 et 255, inclus, ou une référence de cellule qui correspond à un index.</span><span class="sxs-lookup"><span data-stu-id="b8e16-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="b8e16-120">Si _expression_ n’est pas valide, cette fonction renvoie 0 (noir).</span><span class="sxs-lookup"><span data-stu-id="b8e16-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b8e16-121">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b8e16-121">Example 1</span></span>

<span data-ttu-id="b8e16-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="b8e16-122">RED(22)</span></span>
  
<span data-ttu-id="b8e16-123">Renvoie 51 si le document utilise la palette de couleurs par défaut de Microsoft Office Visio, où le gris foncé a l’index de couleur 22.</span><span class="sxs-lookup"><span data-stu-id="b8e16-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b8e16-124">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b8e16-124">Example 2</span></span>

<span data-ttu-id="b8e16-125">Red(char.Color)</span><span class="sxs-lookup"><span data-stu-id="b8e16-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="b8e16-126">Renvoie la valeur de la composante rouge de la couleur de police actuelle.</span><span class="sxs-lookup"><span data-stu-id="b8e16-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b8e16-127">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b8e16-127">Example 3</span></span>

<span data-ttu-id="b8e16-128">RED(RVB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="b8e16-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="b8e16-129">Renvoie 10.</span><span class="sxs-lookup"><span data-stu-id="b8e16-129">Returns 10.</span></span>
  

