---
title: LookupRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloc de données RechercherEnregistrement effectue un ensemble d'actions sur un enregistrement spécifique.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434360"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="d12ae-103">LookupRecord Data Block (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="d12ae-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="d12ae-104">Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="d12ae-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d12ae-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="d12ae-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d12ae-107">Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="d12ae-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d12ae-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d12ae-108">Setting</span></span>

<span data-ttu-id="d12ae-109">L’action **DéfinirChamp** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="d12ae-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="d12ae-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="d12ae-110">**Argument**</span></span>|<span data-ttu-id="d12ae-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d12ae-111">**Required**</span></span>|<span data-ttu-id="d12ae-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="d12ae-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d12ae-113">_In_</span><span class="sxs-lookup"><span data-stu-id="d12ae-113">_In_</span></span> <br/> |<span data-ttu-id="d12ae-114">Oui</span><span class="sxs-lookup"><span data-stu-id="d12ae-114">Yes</span></span>  <br/> |<span data-ttu-id="d12ae-115">Chaîne qui identifie l’enregistrement sur lequel opérer.</span><span class="sxs-lookup"><span data-stu-id="d12ae-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="d12ae-116">*L’argument In* peut contenir le nom de la table, une requête Select ou une SQL instruction.</span><span class="sxs-lookup"><span data-stu-id="d12ae-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="d12ae-117">_Condition Where_</span><span class="sxs-lookup"><span data-stu-id="d12ae-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="d12ae-118">Non</span><span class="sxs-lookup"><span data-stu-id="d12ae-118">No</span></span>  <br/> |<span data-ttu-id="d12ae-119">Expression de type Chaîne qui permet de restreindre la plage de données sur laquelle opère le bloc de données **RechercherEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="d12ae-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="d12ae-120">Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="d12ae-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="d12ae-121">Si des critères sont omis, le bloc de données **LookupRecord** fonctionne sur l’intégralité du domaine spécifié par l’argument *In.*</span><span class="sxs-lookup"><span data-stu-id="d12ae-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="d12ae-122">Tout champ inclus dans les critères doit également être un champ *dans .*</span><span class="sxs-lookup"><span data-stu-id="d12ae-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="d12ae-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="d12ae-123">_Alias_</span></span> <br/> |<span data-ttu-id="d12ae-124">Non</span><span class="sxs-lookup"><span data-stu-id="d12ae-124">No</span></span>  <br/> |<span data-ttu-id="d12ae-125">Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument *In.*</span><span class="sxs-lookup"><span data-stu-id="d12ae-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="d12ae-126">On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës.</span><span class="sxs-lookup"><span data-stu-id="d12ae-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="d12ae-127">Si  *l’alias*  n’est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="d12ae-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d12ae-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="d12ae-128">Remarks</span></span>

<span data-ttu-id="d12ae-129">Si les critères spécifiés par les arguments  *In*  et  *Condition WHERE*  spécifient plusieurs enregistrements, le bloc de données **RechercherEnregistrement** n'opère que sur le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d12ae-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="d12ae-130">Si aucun enregistrement ne satisfait à la *condition Where* ou si *In* ne contient aucun enregistrement, **LookupRecord** crée un enregistrement vide dans lequel tous les champs contiennent une **valeur Null.**</span><span class="sxs-lookup"><span data-stu-id="d12ae-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

