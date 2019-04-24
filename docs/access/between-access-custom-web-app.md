---
title: ENTRE (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Spécifie une plage à tester.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280742"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="e7b04-103">ENTRE (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="e7b04-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="e7b04-104">Spécifie une plage à tester.</span><span class="sxs-lookup"><span data-stu-id="e7b04-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e7b04-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="e7b04-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e7b04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7b04-107">Syntax</span></span>

 <span data-ttu-id="e7b04-108">*test_expression*  AUCUN **Entre** *début_expression* **Et** *fin_expression*</span><span class="sxs-lookup"><span data-stu-id="e7b04-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="e7b04-109">L'opérateur **between** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e7b04-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="e7b04-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="e7b04-110">**Argument**</span></span>|<span data-ttu-id="e7b04-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e7b04-111">**Required**</span></span>|<span data-ttu-id="e7b04-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="e7b04-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e7b04-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="e7b04-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="e7b04-114">Oui</span><span class="sxs-lookup"><span data-stu-id="e7b04-114">Yes</span></span>  <br/> |<span data-ttu-id="e7b04-115">Expression à tester dans la plage définie par les valeurs *début_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="e7b04-116">Doit être du même type de données que *début_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="e7b04-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="e7b04-117">*NOT*</span></span>  <br/> |<span data-ttu-id="e7b04-118">Non</span><span class="sxs-lookup"><span data-stu-id="e7b04-118">No</span></span>  <br/> |<span data-ttu-id="e7b04-119">Spécifie que le résultat du prédicat doit être inversé.</span><span class="sxs-lookup"><span data-stu-id="e7b04-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="e7b04-120">*début_expression*</span><span class="sxs-lookup"><span data-stu-id="e7b04-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="e7b04-121">Oui</span><span class="sxs-lookup"><span data-stu-id="e7b04-121">Yes</span></span>  <br/> |<span data-ttu-id="e7b04-122">Expression valide.</span><span class="sxs-lookup"><span data-stu-id="e7b04-122">A valid expression.</span></span> <span data-ttu-id="e7b04-123">Doit être le même type de données que *test_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="e7b04-124">*fin_expression*</span><span class="sxs-lookup"><span data-stu-id="e7b04-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="e7b04-125">Oui</span><span class="sxs-lookup"><span data-stu-id="e7b04-125">Yes</span></span>  <br/> |<span data-ttu-id="e7b04-126">Expression valide.</span><span class="sxs-lookup"><span data-stu-id="e7b04-126">A valid expression.</span></span> <span data-ttu-id="e7b04-127">Doit être le même type de données que *test_expression* et *début_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="e7b04-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="e7b04-128">*AND*</span></span>  <br/> |<span data-ttu-id="e7b04-129">Oui</span><span class="sxs-lookup"><span data-stu-id="e7b04-129">Yes</span></span>  <br/> |<span data-ttu-id="e7b04-130">Indique que *test_expression* doit être compris dans la plage indiquée par *début_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="e7b04-131">Type de résultat</span><span class="sxs-lookup"><span data-stu-id="e7b04-131">Result Type</span></span>

 <span data-ttu-id="e7b04-132">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="e7b04-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7b04-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7b04-133">Remarks</span></span>

 <span data-ttu-id="e7b04-134">**Between** renvoie **true** si la valeur de *test_expression* est supérieure ou égale à la valeur de *début_expression* et inférieure ou égale à la valeur de *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="e7b04-135">**Not between** renvoie **true** si la valeur de *test_expression* est inférieure à la valeur de *début_expression* ou supérieure à celle de *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="e7b04-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="e7b04-136">Pour spécifier une plage exclusive, utilisez les opérateurs supérieur à\>() et inférieur à (\<).</span><span class="sxs-lookup"><span data-stu-id="e7b04-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

