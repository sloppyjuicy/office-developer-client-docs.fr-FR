---
title: Bloc de données RechercherEnregistrement (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloc de données RechercherEnregistrement effectue un ensemble d'actions sur un enregistrement spécifique.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304269"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="15e78-103">Bloc de données RechercherEnregistrement (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="15e78-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="15e78-104">Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="15e78-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="15e78-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="15e78-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15e78-107">Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="15e78-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="15e78-108">Setting</span><span class="sxs-lookup"><span data-stu-id="15e78-108">Setting</span></span>

<span data-ttu-id="15e78-109">L’action **DéfinirChamp** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="15e78-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="15e78-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="15e78-110">**Argument**</span></span>|<span data-ttu-id="15e78-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="15e78-111">**Required**</span></span>|<span data-ttu-id="15e78-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="15e78-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="15e78-113">_Dans_</span><span class="sxs-lookup"><span data-stu-id="15e78-113">_In_</span></span> <br/> |<span data-ttu-id="15e78-114">Oui</span><span class="sxs-lookup"><span data-stu-id="15e78-114">Yes</span></span>  <br/> |<span data-ttu-id="15e78-115">Chaîne qui identifie l’enregistrement sur lequel opérer.</span><span class="sxs-lookup"><span data-stu-id="15e78-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="15e78-116">L'argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="15e78-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="15e78-117">_Condition Where_</span><span class="sxs-lookup"><span data-stu-id="15e78-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="15e78-118">Non</span><span class="sxs-lookup"><span data-stu-id="15e78-118">No</span></span>  <br/> |<span data-ttu-id="15e78-119">Expression de type Chaîne qui permet de restreindre la plage de données sur laquelle opère le bloc de données **RechercherEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="15e78-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="15e78-120">Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="15e78-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="15e78-121">En cas d'omission de critère, le bloc de données **RechercherEnregistrement** opère sur tout le domaine spécifié par l'argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="15e78-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="15e78-122">Tout champ inclus dans le critère doit également être un champ dans. \*\*</span><span class="sxs-lookup"><span data-stu-id="15e78-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="15e78-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="15e78-123">_Alias_</span></span> <br/> |<span data-ttu-id="15e78-124">Non</span><span class="sxs-lookup"><span data-stu-id="15e78-124">No</span></span>  <br/> |<span data-ttu-id="15e78-125">Chaîne qui fournit un autre nom pour l'enregistrement spécifié par l'argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="15e78-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="15e78-126">On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës.</span><span class="sxs-lookup"><span data-stu-id="15e78-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="15e78-127">Si *alias* n'est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="15e78-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15e78-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="15e78-128">Remarks</span></span>

<span data-ttu-id="15e78-129">Si les critères spécifiés par les arguments  *In*  et  *Condition WHERE*  spécifient plusieurs enregistrements, le bloc de données **RechercherEnregistrement** n'opère que sur le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="15e78-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="15e78-130">Si aucun enregistrement ne satisfait à la *condition WHERE* ou si *in* ne contient aucun enregistrement, **RechercherEnregistrement** crée un enregistrement vide dans lequel tous les champs contiennent une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="15e78-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

