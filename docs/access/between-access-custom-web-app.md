---
title: ENTRE (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Spécifie une plage à tester.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781826"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="34e07-103">ENTRE (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="34e07-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="34e07-104">Spécifie une plage à tester.</span><span class="sxs-lookup"><span data-stu-id="34e07-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="34e07-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="34e07-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="34e07-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34e07-107">Syntax</span></span>

 <span data-ttu-id="34e07-108">*test_expression*  [NOT] **BETWEEN** *begin_expression* **Et** *fin_expression*</span><span class="sxs-lookup"><span data-stu-id="34e07-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="34e07-109">L’opérateur **Between** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="34e07-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="34e07-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="34e07-110">**Argument**</span></span>|<span data-ttu-id="34e07-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="34e07-111">**Required**</span></span>|<span data-ttu-id="34e07-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="34e07-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="34e07-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="34e07-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="34e07-114">Oui</span><span class="sxs-lookup"><span data-stu-id="34e07-114">Yes</span></span>  <br/> |<span data-ttu-id="34e07-115">Expression à tester dans la plage définie par les *paramètres début_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="34e07-116">Doit être du même type que *début_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="34e07-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="34e07-117">*NOT*</span></span>  <br/> |<span data-ttu-id="34e07-118">Non</span><span class="sxs-lookup"><span data-stu-id="34e07-118">No</span></span>  <br/> |<span data-ttu-id="34e07-119">Spécifie que le résultat du prédicat est inversée.</span><span class="sxs-lookup"><span data-stu-id="34e07-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="34e07-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="34e07-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="34e07-121">Oui</span><span class="sxs-lookup"><span data-stu-id="34e07-121">Yes</span></span>  <br/> |<span data-ttu-id="34e07-122">Une expression valide.</span><span class="sxs-lookup"><span data-stu-id="34e07-122">A valid expression.</span></span> <span data-ttu-id="34e07-123">Doit être le même type de données que *test_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="34e07-124">*fin_expression*</span><span class="sxs-lookup"><span data-stu-id="34e07-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="34e07-125">Oui</span><span class="sxs-lookup"><span data-stu-id="34e07-125">Yes</span></span>  <br/> |<span data-ttu-id="34e07-126">Une expression valide.</span><span class="sxs-lookup"><span data-stu-id="34e07-126">A valid expression.</span></span> <span data-ttu-id="34e07-127">Doit être du même type que *test_expression* et *début_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="34e07-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="34e07-128">*AND*</span></span>  <br/> |<span data-ttu-id="34e07-129">Oui</span><span class="sxs-lookup"><span data-stu-id="34e07-129">Yes</span></span>  <br/> |<span data-ttu-id="34e07-130">Indique que *test_expression* doit se trouver dans la plage indiquée par les *paramètres début_expression* et *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="34e07-131">Type de résultat</span><span class="sxs-lookup"><span data-stu-id="34e07-131">Result Type</span></span>

 <span data-ttu-id="34e07-132">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="34e07-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34e07-133">Notes</span><span class="sxs-lookup"><span data-stu-id="34e07-133">Remarks</span></span>

 <span data-ttu-id="34e07-134">**BETWEEN** renvoie **la valeur TRUE** si la valeur de *test_expression* est supérieure ou égale à celle de *début_expression* et inférieure ou égale à celle de *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="34e07-135">**NOT BETWEEN** renvoie **la valeur TRUE** si la valeur de *test_expression* est inférieure à celle de *début_expression* ou supérieure à celle de *fin_expression* .</span><span class="sxs-lookup"><span data-stu-id="34e07-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="34e07-136">Pour spécifier un intervalle exclusif, utilisez la plus grande que (\>) et inférieur à opérateurs (\<).</span><span class="sxs-lookup"><span data-stu-id="34e07-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

