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
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348950"
---
# <a name="bound-function"></a><span data-ttu-id="a97ce-103">Fonction BOUND</span><span class="sxs-lookup"><span data-stu-id="a97ce-103">BOUND Function</span></span>

<span data-ttu-id="a97ce-104">Limite la valeur d’une cellule à une plage ou à un ensemble de plages.</span><span class="sxs-lookup"><span data-stu-id="a97ce-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a97ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a97ce-105">Syntax</span></span>

<span data-ttu-id="a97ce-106">BOUND (\* \* *value* \* \*, \* \* *type* \* \*, \* \* *ignore* \* \*, \* \* *value1* \* \*, \* \* *value2* \* \* \* \* \* [, ignore (n), value1 (n), valeur2 (n),...] \* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a97ce-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a97ce-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a97ce-107">Parameters</span></span>

|<span data-ttu-id="a97ce-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a97ce-108">**Name**</span></span>|<span data-ttu-id="a97ce-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a97ce-109">**Required/Optional**</span></span>|<span data-ttu-id="a97ce-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a97ce-110">**Data Type**</span></span>|<span data-ttu-id="a97ce-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a97ce-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a97ce-112">_value_</span><span class="sxs-lookup"><span data-stu-id="a97ce-112">_value_</span></span> <br/> |<span data-ttu-id="a97ce-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a97ce-113">Required</span></span>  <br/> |<span data-ttu-id="a97ce-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a97ce-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a97ce-115">Valeur actuelle limitée.</span><span class="sxs-lookup"><span data-stu-id="a97ce-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="a97ce-116">_type_</span><span class="sxs-lookup"><span data-stu-id="a97ce-116">_type_</span></span> <br/> |<span data-ttu-id="a97ce-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a97ce-117">Required</span></span>  <br/> |<span data-ttu-id="a97ce-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a97ce-118">**Numeric**</span></span> <br/> |<span data-ttu-id="a97ce-119">Indique si la contrainte est inclusive (0), exclusive (1) ou désactivée (2).</span><span class="sxs-lookup"><span data-stu-id="a97ce-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="a97ce-120">_Passez_</span><span class="sxs-lookup"><span data-stu-id="a97ce-120">_ignore_</span></span> <br/> |<span data-ttu-id="a97ce-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a97ce-121">Required</span></span>  <br/> |<span data-ttu-id="a97ce-122">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="a97ce-122">**Boolean**</span></span> <br/> | <span data-ttu-id="a97ce-123">TRUE pour ignorer la plage; FALSe pour limiter la valeur de la cellule à la plage.</span><span class="sxs-lookup"><span data-stu-id="a97ce-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="a97ce-124">_valeur1,valeur2_</span><span class="sxs-lookup"><span data-stu-id="a97ce-124">_value1_</span></span> <br/> |<span data-ttu-id="a97ce-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a97ce-125">Required</span></span>  <br/> |<span data-ttu-id="a97ce-126">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a97ce-126">**Numeric**</span></span> <br/> |<span data-ttu-id="a97ce-127">Première valeur d’une plage.</span><span class="sxs-lookup"><span data-stu-id="a97ce-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="a97ce-128">_valeur2_</span><span class="sxs-lookup"><span data-stu-id="a97ce-128">_value2_</span></span> <br/> |<span data-ttu-id="a97ce-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a97ce-129">Required</span></span>  <br/> |<span data-ttu-id="a97ce-130">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a97ce-130">**Numeric**</span></span> <br/> |<span data-ttu-id="a97ce-131">Deuxième valeur d’une plage.</span><span class="sxs-lookup"><span data-stu-id="a97ce-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a97ce-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="a97ce-132">Remarks</span></span>

<span data-ttu-id="a97ce-133">Utilisez la fonction BOUND pour restreindre la valeur d’une cellule à une limite supérieure et inférieure, par exemple, pour contrôler des objets qui ne devraient pas être étirés au delà ou en deçà d’une hauteur minimale ou maximale.</span><span class="sxs-lookup"><span data-stu-id="a97ce-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="a97ce-134">La contrainte peut être inclusive ou exclusive par rapport aux plages.</span><span class="sxs-lookup"><span data-stu-id="a97ce-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="a97ce-135">Si la valeur actuelle ne doit pas être restreinte, définissez le paramètre _type_ sur 2 (Disabled).</span><span class="sxs-lookup"><span data-stu-id="a97ce-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="a97ce-136">Vous pouvez définir plusieurs plages en fournissant plusieurs occurrences des paramètres _ignore_, _value1_et _value2_ .</span><span class="sxs-lookup"><span data-stu-id="a97ce-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="a97ce-137">Utilisez le __ paramètre ignore pour désactiver les contraintes d'une plage particulière.</span><span class="sxs-lookup"><span data-stu-id="a97ce-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="a97ce-138">La formule contenant la fonction BOUND n'est pas remplacée lorsque sa valeur change; au lieu de cela, la formule est conservée et la nouvelle valeur est placée dans le paramètre _value_ .</span><span class="sxs-lookup"><span data-stu-id="a97ce-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a97ce-139">Exemple1</span><span class="sxs-lookup"><span data-stu-id="a97ce-139">Example 1</span></span>

<span data-ttu-id="a97ce-140">Cet exemple utilise la fonction BOUND pour obliger une poignée de contrôle à rester à l’intérieur du rectangle de délimitation d’une forme.</span><span class="sxs-lookup"><span data-stu-id="a97ce-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="a97ce-141">Controls. X1 = BOUND (\*largeur 0,5, 0, faux,\*largeur 0,\*largeur 1)</span><span class="sxs-lookup"><span data-stu-id="a97ce-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="a97ce-142">Controls. Y1 = BOUND (\*hauteur 0,5, 0, false\*, hauteur 0\*, hauteur 1)</span><span class="sxs-lookup"><span data-stu-id="a97ce-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a97ce-143">Exemple2</span><span class="sxs-lookup"><span data-stu-id="a97ce-143">Example 2</span></span>

<span data-ttu-id="a97ce-144">Cet exemple utilise la fonction BOUND pour limiter la largeur d’une forme à 2 pouces, 4 pouces ou 6 pouces.</span><span class="sxs-lookup"><span data-stu-id="a97ce-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="a97ce-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="a97ce-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

