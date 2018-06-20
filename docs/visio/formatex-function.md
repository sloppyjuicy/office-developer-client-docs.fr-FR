---
title: FORMATEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Renvoie le résultat d’expression calculé en unité srcUnit sous forme de chaîne mise en forme selon le format exprimé en dstUnit.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788692"
---
# <a name="formatex-function"></a><span data-ttu-id="828c1-103">FORMATEX, fonction</span><span class="sxs-lookup"><span data-stu-id="828c1-103">FORMATEX Function</span></span>

<span data-ttu-id="828c1-104">Renvoie le résultat d’expression calculé en unité srcUnit sous forme de chaîne mise en forme selon le format exprimé en dstUnit.</span><span class="sxs-lookup"><span data-stu-id="828c1-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="828c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="828c1-105">Syntax</span></span>

<span data-ttu-id="828c1-106">FORMATEX (** *expression* **, « ** *format* ** », [** *srcUnit* **], [** *dstUnit* **], [** *langID* **] [, ** *calID* **])</span><span class="sxs-lookup"><span data-stu-id="828c1-106">FORMATEX(** *expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="828c1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="828c1-107">Parameters</span></span>

|<span data-ttu-id="828c1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="828c1-108">**Name**</span></span>|<span data-ttu-id="828c1-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="828c1-109">**Required/Optional**</span></span>|<span data-ttu-id="828c1-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="828c1-110">**Data Type**</span></span>|<span data-ttu-id="828c1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="828c1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="828c1-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="828c1-112">_expression_</span></span> <br/> |<span data-ttu-id="828c1-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="828c1-113">Required</span></span>  <br/> |<span data-ttu-id="828c1-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="828c1-114">**String**</span></span> <br/> |<span data-ttu-id="828c1-115">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.</span><span class="sxs-lookup"><span data-stu-id="828c1-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="828c1-116">_format_</span><span class="sxs-lookup"><span data-stu-id="828c1-116">_format_</span></span> <br/> |<span data-ttu-id="828c1-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="828c1-117">Required</span></span>  <br/> |<span data-ttu-id="828c1-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="828c1-118">**String**</span></span> <br/> |<span data-ttu-id="828c1-119">Le format de l’image utilisée pour la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="828c1-119">The format picture used to format the string.</span></span> <span data-ttu-id="828c1-120">Pour plus d’informations sur les modèles de format, consultez la rubrique [Sur les modèles de Format](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="828c1-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="828c1-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="828c1-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="828c1-122">Facultatif</span><span class="sxs-lookup"><span data-stu-id="828c1-122">Optional</span></span>  <br/> |<span data-ttu-id="828c1-123">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="828c1-123">**String**</span></span> <br/> | <span data-ttu-id="828c1-124">Unités utilisées pour calculer expression (po, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="828c1-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="828c1-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="828c1-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="828c1-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="828c1-126">Optional</span></span>  <br/> |<span data-ttu-id="828c1-127">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="828c1-127">**String**</span></span> <br/> |<span data-ttu-id="828c1-128">Unités à utiliser pour le résultat d’expression (po, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="828c1-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="828c1-129">_ID de langue_</span><span class="sxs-lookup"><span data-stu-id="828c1-129">_langID_</span></span> <br/> |<span data-ttu-id="828c1-130">Facultatif</span><span class="sxs-lookup"><span data-stu-id="828c1-130">Optional</span></span>  <br/> |<span data-ttu-id="828c1-131">**Number**</span><span class="sxs-lookup"><span data-stu-id="828c1-131">**Number**</span></span> <br/> |<span data-ttu-id="828c1-132">Langue utilisée lors de la mise en forme des dates/heures de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="828c1-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="828c1-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="828c1-133">_calID_</span></span> <br/> |<span data-ttu-id="828c1-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="828c1-134">Optional</span></span>  <br/> |<span data-ttu-id="828c1-135">**Number**</span><span class="sxs-lookup"><span data-stu-id="828c1-135">**Number**</span></span> <br/> |<span data-ttu-id="828c1-136">Calendrier utilisé lors de la mise en forme des dates/heures de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="828c1-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="828c1-137">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="828c1-137">Return value</span></span>

<span data-ttu-id="828c1-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="828c1-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="828c1-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="828c1-139">Remarks</span></span>

<span data-ttu-id="828c1-140">Le type de l’expression et le type spécifié dans le modèle de format régissent le comportement de la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="828c1-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="828c1-141">Le format doit être approprié pour le type d’expression.</span><span class="sxs-lookup"><span data-stu-id="828c1-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="828c1-142">L’argument srcUnit est utilisé à l’échelle des résultats d’expressions non typées, telles que 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="828c1-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="828c1-143">Si le résultat d’expression est un type explicite, tel que 3 ft + 8 ft, l’argument srcUnit est ignoré.</span><span class="sxs-lookup"><span data-stu-id="828c1-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="828c1-144">L’argument dstUnit est utilisé pour spécifier les unités utilisées pour le résultat de la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="828c1-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="828c1-145">Si dstUnit n’est pas spécifié, les unités pour le résultat de l’expression sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="828c1-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="828c1-146">Renvoie une erreur si le résultat de l’expression et le type attendu dans format est de même nature, s’il existe des erreurs de syntaxe dans format, ou si elle ne reconnaît pas les unités transmise dans les arguments srcUnit ou dstUnit.</span><span class="sxs-lookup"><span data-stu-id="828c1-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="828c1-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="828c1-147">Example</span></span>

<span data-ttu-id="828c1-148">FORMATEX(5,5, "0,00 u", "cm", "m")</span><span class="sxs-lookup"><span data-stu-id="828c1-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="828c1-149">Renvoie 0,06 mètre.</span><span class="sxs-lookup"><span data-stu-id="828c1-149">Returns 0.18 feet.</span></span> 
  

