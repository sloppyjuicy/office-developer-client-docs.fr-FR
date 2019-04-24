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
description: Renvoie le résultat d'expression évaluée dans srcUnit sous forme de chaîne mise en forme selon le format exprimé en dstUnit.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328629"
---
# <a name="formatex-function"></a><span data-ttu-id="dde06-103">Fonction FORMATEX</span><span class="sxs-lookup"><span data-stu-id="dde06-103">FORMATEX Function</span></span>

<span data-ttu-id="dde06-104">Renvoie le résultat d'expression évaluée dans srcUnit sous forme de chaîne mise en forme selon le format exprimé en dstUnit.</span><span class="sxs-lookup"><span data-stu-id="dde06-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dde06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dde06-105">Syntax</span></span>

<span data-ttu-id="dde06-106">FORMATEX (\* \* *expression* \* *, "* \* *format* \* *", [* \* *srcUnit* \* *], [* \* *dstUnit* \* *], [* \* *LangID* \* \*] [, \* \* *calID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="dde06-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dde06-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dde06-107">Parameters</span></span>

|<span data-ttu-id="dde06-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dde06-108">**Name**</span></span>|<span data-ttu-id="dde06-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="dde06-109">**Required/Optional**</span></span>|<span data-ttu-id="dde06-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="dde06-110">**Data Type**</span></span>|<span data-ttu-id="dde06-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="dde06-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dde06-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="dde06-112">_expression_</span></span> <br/> |<span data-ttu-id="dde06-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dde06-113">Required</span></span>  <br/> |<span data-ttu-id="dde06-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dde06-114">**String**</span></span> <br/> |<span data-ttu-id="dde06-115">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.</span><span class="sxs-lookup"><span data-stu-id="dde06-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="dde06-116">_format_</span><span class="sxs-lookup"><span data-stu-id="dde06-116">_format_</span></span> <br/> |<span data-ttu-id="dde06-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dde06-117">Required</span></span>  <br/> |<span data-ttu-id="dde06-118">**String**</span><span class="sxs-lookup"><span data-stu-id="dde06-118">**String**</span></span> <br/> |<span data-ttu-id="dde06-119">Image de format utilisée pour mettre en forme la chaîne.</span><span class="sxs-lookup"><span data-stu-id="dde06-119">The format picture used to format the string.</span></span> <span data-ttu-id="dde06-120">Pour plus d'informations sur la mise en forme des images, voir [à propos](about-format-pictures.md)de la mise en forme des images.</span><span class="sxs-lookup"><span data-stu-id="dde06-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="dde06-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="dde06-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="dde06-122">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dde06-122">Optional</span></span>  <br/> |<span data-ttu-id="dde06-123">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="dde06-123">**String**</span></span> <br/> | <span data-ttu-id="dde06-124">Unités utilisées pour calculer expression (po, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="dde06-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="dde06-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="dde06-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="dde06-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dde06-126">Optional</span></span>  <br/> |<span data-ttu-id="dde06-127">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="dde06-127">**String**</span></span> <br/> |<span data-ttu-id="dde06-128">Unités à utiliser pour le résultat d’expression (po, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="dde06-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="dde06-129">_ID_</span><span class="sxs-lookup"><span data-stu-id="dde06-129">_langID_</span></span> <br/> |<span data-ttu-id="dde06-130">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dde06-130">Optional</span></span>  <br/> |<span data-ttu-id="dde06-131">**Number**</span><span class="sxs-lookup"><span data-stu-id="dde06-131">**Number**</span></span> <br/> |<span data-ttu-id="dde06-132">Langue utilisée lors de la mise en forme des dates/heures de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="dde06-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="dde06-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="dde06-133">_calID_</span></span> <br/> |<span data-ttu-id="dde06-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dde06-134">Optional</span></span>  <br/> |<span data-ttu-id="dde06-135">**Number**</span><span class="sxs-lookup"><span data-stu-id="dde06-135">**Number**</span></span> <br/> |<span data-ttu-id="dde06-136">Calendrier utilisé lors de la mise en forme des dates/heures de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="dde06-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dde06-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dde06-137">Return value</span></span>

<span data-ttu-id="dde06-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dde06-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dde06-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="dde06-139">Remarks</span></span>

<span data-ttu-id="dde06-140">Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="dde06-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="dde06-141">L’argument format doit convenir au type de l’expression.</span><span class="sxs-lookup"><span data-stu-id="dde06-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="dde06-142">L’argument srcUnit est utilisé pour mettre à l’échelle des résultats d’expressions non typées, telles que 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="dde06-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="dde06-143">Si le résultat d’expression est associé à un type précis, comme 3 m + 8 m, l’argument srcUnit est ignoré.</span><span class="sxs-lookup"><span data-stu-id="dde06-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="dde06-144">L’argument dstUnit est utilisé pour définir les unités employées dans le résultat mis en forme.</span><span class="sxs-lookup"><span data-stu-id="dde06-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="dde06-145">Si dstUnit n’est pas précisé, les unités du résultat de l’expression sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="dde06-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="dde06-146">Renvoie une erreur si le résultat d’expression et le type attendu dans format ne sont pas de même nature, si des erreurs de syntaxe se sont glissées dans format ou si les unités transmises dans les arguments srcUnit ou dstUnit ne sont pas reconnues.</span><span class="sxs-lookup"><span data-stu-id="dde06-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="dde06-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="dde06-147">Example</span></span>

<span data-ttu-id="dde06-148">FORMATEX(5,5, "0,00 u", "cm", "m")</span><span class="sxs-lookup"><span data-stu-id="dde06-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="dde06-149">Renvoie 0,06 mètre.</span><span class="sxs-lookup"><span data-stu-id="dde06-149">Returns 0.18 feet.</span></span> 
  

