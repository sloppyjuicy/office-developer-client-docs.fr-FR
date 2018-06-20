---
title: BOUND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Limite la valeur d’une cellule à une plage ou à un ensemble de plages.
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788195"
---
# <a name="bound-function"></a><span data-ttu-id="a65c6-103">BOUND, fonction</span><span class="sxs-lookup"><span data-stu-id="a65c6-103">BOUND Function</span></span>

<span data-ttu-id="a65c6-104">Limite la valeur d’une cellule à une plage ou à un ensemble de plages.</span><span class="sxs-lookup"><span data-stu-id="a65c6-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a65c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a65c6-105">Syntax</span></span>

<span data-ttu-id="a65c6-106">LIÉ (** *valeur* **, ** *type* **, ** *Ignorer* **, ** *valeur1* **, ** *valeur2* ** ** * [, ignore(n), value1(n), value2(n),...] * **)</span><span class="sxs-lookup"><span data-stu-id="a65c6-106">BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a65c6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a65c6-107">Parameters</span></span>

|<span data-ttu-id="a65c6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a65c6-108">**Name**</span></span>|<span data-ttu-id="a65c6-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a65c6-109">**Required/Optional**</span></span>|<span data-ttu-id="a65c6-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a65c6-110">**Data Type**</span></span>|<span data-ttu-id="a65c6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a65c6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a65c6-112">_valeur_</span><span class="sxs-lookup"><span data-stu-id="a65c6-112">_value_</span></span> <br/> |<span data-ttu-id="a65c6-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a65c6-113">Required</span></span>  <br/> |<span data-ttu-id="a65c6-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a65c6-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a65c6-115">Valeur actuelle limitée.</span><span class="sxs-lookup"><span data-stu-id="a65c6-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="a65c6-116">_type_</span><span class="sxs-lookup"><span data-stu-id="a65c6-116">_type_</span></span> <br/> |<span data-ttu-id="a65c6-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a65c6-117">Required</span></span>  <br/> |<span data-ttu-id="a65c6-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a65c6-118">**Numeric**</span></span> <br/> |<span data-ttu-id="a65c6-119">Si la contrainte est inclusive (0), exclusive (1) ou désactivée (2).</span><span class="sxs-lookup"><span data-stu-id="a65c6-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="a65c6-120">_Ignorer_</span><span class="sxs-lookup"><span data-stu-id="a65c6-120">_ignore_</span></span> <br/> |<span data-ttu-id="a65c6-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a65c6-121">Required</span></span>  <br/> |<span data-ttu-id="a65c6-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a65c6-122">**Boolean**</span></span> <br/> | <span data-ttu-id="a65c6-123">TRUE pour ignorer la plage ; Valeur FALSE pour limiter la valeur de la cellule à la plage.</span><span class="sxs-lookup"><span data-stu-id="a65c6-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="a65c6-124">_valeur1_</span><span class="sxs-lookup"><span data-stu-id="a65c6-124">_value1_</span></span> <br/> |<span data-ttu-id="a65c6-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a65c6-125">Required</span></span>  <br/> |<span data-ttu-id="a65c6-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a65c6-126">**Numeric**</span></span> <br/> |<span data-ttu-id="a65c6-127">Première valeur dans une plage.</span><span class="sxs-lookup"><span data-stu-id="a65c6-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="a65c6-128">_valeur2_</span><span class="sxs-lookup"><span data-stu-id="a65c6-128">_value2_</span></span> <br/> |<span data-ttu-id="a65c6-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a65c6-129">Required</span></span>  <br/> |<span data-ttu-id="a65c6-130">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a65c6-130">**Numeric**</span></span> <br/> |<span data-ttu-id="a65c6-131">Deuxième valeur d’une plage.</span><span class="sxs-lookup"><span data-stu-id="a65c6-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a65c6-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="a65c6-132">Remarks</span></span>

<span data-ttu-id="a65c6-133">Utilisez la fonction BOUND pour restreindre la valeur à une limite supérieure d’une cellule et limite inférieure, par exemple, pour contrôler des objets qui ne doivent pas être étirés au-dessus ou au-dessous d’une hauteur minimale ou maximale.</span><span class="sxs-lookup"><span data-stu-id="a65c6-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="a65c6-134">La contrainte peut être inclus ou exclus en ce qui concerne l’ou les plages.</span><span class="sxs-lookup"><span data-stu-id="a65c6-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="a65c6-135">Si la valeur actuelle ne doit pas être limitée, définissez le paramètre _type_ sur 2 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="a65c6-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="a65c6-136">Vous pouvez définir plusieurs plages en fournissant plusieurs occurrences des paramètres _ignore_, _value1_et _value2_ .</span><span class="sxs-lookup"><span data-stu-id="a65c6-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="a65c6-137">Pour désactiver des contraintes à une plage donnée, utilisez le paramètre _Ignorer_ .</span><span class="sxs-lookup"><span data-stu-id="a65c6-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="a65c6-138">La formule contenant la fonction BOUND n’est pas écrasée lorsque sa valeur change ; au lieu de cela, la formule est préservée et la nouvelle valeur est placée dans le paramètre _value_ .</span><span class="sxs-lookup"><span data-stu-id="a65c6-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a65c6-139">Exemple1</span><span class="sxs-lookup"><span data-stu-id="a65c6-139">Example 1</span></span>

<span data-ttu-id="a65c6-140">Cet exemple utilise la fonction BOUND pour obliger une poignée de contrôle à rester à l’intérieur du rectangle de délimitation d’une forme.</span><span class="sxs-lookup"><span data-stu-id="a65c6-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="a65c6-141">Controls.X1 = liés aux (largeur\*0,5, 0, la valeur FALSE, la largeur\*largeur 0,\*1)</span><span class="sxs-lookup"><span data-stu-id="a65c6-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="a65c6-142">Controls.Y1 = liés aux (hauteur\*0,5, 0, la valeur FALSE, la hauteur\*hauteur 0,\*1)</span><span class="sxs-lookup"><span data-stu-id="a65c6-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a65c6-143">Exemple2</span><span class="sxs-lookup"><span data-stu-id="a65c6-143">Example 2</span></span>

<span data-ttu-id="a65c6-144">Cet exemple utilise la fonction BOUND pour limiter la largeur d’une forme à 2 pouces, 4 pouces ou 6 pouces.</span><span class="sxs-lookup"><span data-stu-id="a65c6-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="a65c6-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="a65c6-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

