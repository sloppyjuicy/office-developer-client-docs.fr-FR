---
title: Bloc de données PourChaqueEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloc de données PourChaqueEnregistrement répète un ensemble d’instructions pour chaque enregistrement dans un domaine.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781836"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="e1804-103">Bloc de données PourChaqueEnregistrement (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="e1804-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="e1804-104">Un bloc de données **PourChaqueEnregistrement** répète un ensemble d’instructions pour chaque enregistrement dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="e1804-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e1804-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="e1804-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1804-107">Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="e1804-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="e1804-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e1804-108">Setting</span></span>

<span data-ttu-id="e1804-109">L'action **PourChaqueEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e1804-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="e1804-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="e1804-110">**Argument name**</span></span>|<span data-ttu-id="e1804-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e1804-111">**Required**</span></span>|<span data-ttu-id="e1804-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1804-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1804-113">**Dans**</span><span class="sxs-lookup"><span data-stu-id="e1804-113">**In**</span></span> <br/> |<span data-ttu-id="e1804-114">Oui</span><span class="sxs-lookup"><span data-stu-id="e1804-114">Yes</span></span>  <br/> |<span data-ttu-id="e1804-115">Une chaîne qui identifie le domaine d’enregistrements de fonctionner sur.</span><span class="sxs-lookup"><span data-stu-id="e1804-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="e1804-116">L’argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="e1804-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="e1804-117">**Remarque**: le domaine spécifié ne peut pas inclure les données stockées dans une table liée ou d’une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="e1804-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="e1804-118">**Where Condition**</span><span class="sxs-lookup"><span data-stu-id="e1804-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="e1804-119">Non</span><span class="sxs-lookup"><span data-stu-id="e1804-119">No</span></span>  <br/> |<span data-ttu-id="e1804-120">Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données **PourChaqueEnregistrement** est effectuée.</span><span class="sxs-lookup"><span data-stu-id="e1804-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="e1804-121">Par exemple, critères est souvent équivalent à la clause WHERE d’une expression SQL sans le mot où.</span><span class="sxs-lookup"><span data-stu-id="e1804-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="e1804-122">Si les critères sont tous deux omis, le bloc de données **PourChaqueEnregistrement** opère sur l’intégralité du domaine spécifié par l’argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="e1804-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="e1804-123">Un champ qui est inclus dans les critères doit également être un champ *dans* .</span><span class="sxs-lookup"><span data-stu-id="e1804-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="e1804-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="e1804-124">**Alias**</span></span> <br/> |<span data-ttu-id="e1804-125">Non</span><span class="sxs-lookup"><span data-stu-id="e1804-125">No</span></span>  <br/> |<span data-ttu-id="e1804-126">Chaîne qui fournit un autre nom pour le domaine spécifié par l’argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="e1804-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="e1804-127">Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus.</span><span class="sxs-lookup"><span data-stu-id="e1804-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="e1804-128">Si *Alias* n’est pas spécifié, le nom de la table ou requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="e1804-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1804-129">Notes</span><span class="sxs-lookup"><span data-stu-id="e1804-129">Remarks</span></span>

<span data-ttu-id="e1804-130">Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action-access-custom-web-app.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="e1804-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

