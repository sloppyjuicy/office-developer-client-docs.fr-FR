---
title: PourChaqueEnregistrement, bloc de données (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloc de données PourChaqueEnregistrement répète un ensemble d'instructions pour chaque enregistrement dans un domaine.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302456"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="f62ef-103">PourChaqueEnregistrement, bloc de données (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="f62ef-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="f62ef-104">Un bloc de données **PourChaqueEnregistrement** répète un ensemble d'instructions pour chaque enregistrement dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="f62ef-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f62ef-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f62ef-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f62ef-107">Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="f62ef-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f62ef-108">Setting</span><span class="sxs-lookup"><span data-stu-id="f62ef-108">Setting</span></span>

<span data-ttu-id="f62ef-109">L’action **PourChaqueEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="f62ef-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="f62ef-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="f62ef-110">**Argument name**</span></span>|<span data-ttu-id="f62ef-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f62ef-111">**Required**</span></span>|<span data-ttu-id="f62ef-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="f62ef-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f62ef-113">**Dans**</span><span class="sxs-lookup"><span data-stu-id="f62ef-113">**In**</span></span> <br/> |<span data-ttu-id="f62ef-114">Oui</span><span class="sxs-lookup"><span data-stu-id="f62ef-114">Yes</span></span>  <br/> |<span data-ttu-id="f62ef-115">Chaîne qui identifie le domaine d’enregistrements sur lequel opérer.</span><span class="sxs-lookup"><span data-stu-id="f62ef-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="f62ef-116">L'argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="f62ef-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="f62ef-117">**Remarque**: le domaine spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="f62ef-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="f62ef-118">**Condition Where**</span><span class="sxs-lookup"><span data-stu-id="f62ef-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="f62ef-119">Non</span><span class="sxs-lookup"><span data-stu-id="f62ef-119">No</span></span>  <br/> |<span data-ttu-id="f62ef-120">Expression de chaîne servant à limiter la plage de données sur laquelle le bloc de données **PourChaqueEnregistrement** est exécuté.</span><span class="sxs-lookup"><span data-stu-id="f62ef-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="f62ef-121">Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="f62ef-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="f62ef-122">Si les critères sont omis, le bloc de données **PourChaqueEnregistrement** s'applique à l'ensemble du domaine spécifié par l'argument *in* .</span><span class="sxs-lookup"><span data-stu-id="f62ef-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="f62ef-123">Tout champ inclus dans le critère doit également être un champ dans. \*\*</span><span class="sxs-lookup"><span data-stu-id="f62ef-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="f62ef-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="f62ef-124">**Alias**</span></span> <br/> |<span data-ttu-id="f62ef-125">Non</span><span class="sxs-lookup"><span data-stu-id="f62ef-125">No</span></span>  <br/> |<span data-ttu-id="f62ef-126">Chaîne qui fournit un autre nom pour le domaine spécifié par l'argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="f62ef-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="f62ef-127">On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës.</span><span class="sxs-lookup"><span data-stu-id="f62ef-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="f62ef-128">Si *alias* n'est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="f62ef-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f62ef-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="f62ef-129">Remarks</span></span>

<span data-ttu-id="f62ef-130">Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action-access-custom-web-app.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="f62ef-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

