---
title: Bloc de données RechercherEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloc de données RechercherEnregistrement effectue un ensemble d’actions sur un enregistrement spécifique.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781860"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="8e3e9-103">Bloc de données RechercherEnregistrement (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="8e3e9-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="8e3e9-104">Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8e3e9-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8e3e9-107">[!REMARQUE] Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8e3e9-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8e3e9-108">Setting</span></span>

<span data-ttu-id="8e3e9-109">L'action **DéfinirChamp** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="8e3e9-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="8e3e9-110">**Argument**</span></span>|<span data-ttu-id="8e3e9-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8e3e9-111">**Required**</span></span>|<span data-ttu-id="8e3e9-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="8e3e9-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8e3e9-113">_Dans_</span><span class="sxs-lookup"><span data-stu-id="8e3e9-113">_In_</span></span> <br/> |<span data-ttu-id="8e3e9-114">Oui</span><span class="sxs-lookup"><span data-stu-id="8e3e9-114">Yes</span></span>  <br/> |<span data-ttu-id="8e3e9-115">Une chaîne qui identifie l’enregistrement à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="8e3e9-116">L’argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="8e3e9-117">_Where Condition_</span><span class="sxs-lookup"><span data-stu-id="8e3e9-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="8e3e9-118">Non</span><span class="sxs-lookup"><span data-stu-id="8e3e9-118">No</span></span>  <br/> |<span data-ttu-id="8e3e9-119">Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données **RechercherEnregistrement** est effectuée.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="8e3e9-120">Par exemple, critères est souvent équivalent à la clause WHERE d’une expression SQL sans le mot où.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="8e3e9-121">Si l’argument critères est omis, le bloc de données **RechercherEnregistrement** opère sur l’intégralité du domaine spécifié par l’argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="8e3e9-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="8e3e9-122">Un champ qui est inclus dans les critères doit également être un champ *dans* .</span><span class="sxs-lookup"><span data-stu-id="8e3e9-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="8e3e9-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="8e3e9-123">_Alias_</span></span> <br/> |<span data-ttu-id="8e3e9-124">Non</span><span class="sxs-lookup"><span data-stu-id="8e3e9-124">No</span></span>  <br/> |<span data-ttu-id="8e3e9-125">Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument *dans* .</span><span class="sxs-lookup"><span data-stu-id="8e3e9-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="8e3e9-126">Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="8e3e9-127">Si *Alias* n’est pas spécifié, le nom de la table ou requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e3e9-128">Notes</span><span class="sxs-lookup"><span data-stu-id="8e3e9-128">Remarks</span></span>

<span data-ttu-id="8e3e9-129">Si les critères spécifiés par les arguments  *In*  et  *Condition WHERE*  spécifient plusieurs enregistrements, le bloc de données **RechercherEnregistrement** n'opère que sur le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8e3e9-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="8e3e9-130">Si aucun enregistrement ne satisfait à *Condition Where* ou si *In* ne contient aucun enregistrement, **RechercherEnregistrement** crée un enregistrement vide dans lequel tous les champs contiennent une valeur **Null** .</span><span class="sxs-lookup"><span data-stu-id="8e3e9-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

