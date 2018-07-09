---
title: Action de Macro RequeryRecords (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Vous pouvez utiliser l’action RequeryRecords pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781970"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="2e36a-103">Action de Macro RequeryRecords (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="2e36a-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2e36a-104">Vous pouvez utiliser l’action **RequeryRecords** pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2e36a-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2e36a-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="2e36a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2e36a-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e36a-107">Setting</span></span>

<span data-ttu-id="2e36a-108">L’action **RequeryRecords** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="2e36a-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="2e36a-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="2e36a-109">**Parameter**</span></span>|<span data-ttu-id="2e36a-110">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2e36a-110">**Required**</span></span>|<span data-ttu-id="2e36a-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e36a-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e36a-112">**Où =**</span><span class="sxs-lookup"><span data-stu-id="2e36a-112">**Where=**</span></span> <br/> |<span data-ttu-id="2e36a-113">Non</span><span class="sxs-lookup"><span data-stu-id="2e36a-113">No</span></span>  <br/> |<span data-ttu-id="2e36a-114">Une clause WHERE SQL qui limite les enregistrements dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2e36a-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="2e36a-115">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="2e36a-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="2e36a-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="2e36a-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="2e36a-117">Non</span><span class="sxs-lookup"><span data-stu-id="2e36a-117">No</span></span>  <br/> |<span data-ttu-id="2e36a-118">Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</span><span class="sxs-lookup"><span data-stu-id="2e36a-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="2e36a-119">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="2e36a-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e36a-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e36a-120">Remarks</span></span>

<span data-ttu-id="2e36a-121">Tout tri ou filtrage appliqué par l’utilisateur est effacé lors de l’action **RequeryRecords** est appelée.</span><span class="sxs-lookup"><span data-stu-id="2e36a-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="2e36a-122">L’argument *OrderBy (TriPar)* est le nom du champ ou des champs sur lesquels vous souhaitez trier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="2e36a-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="2e36a-123">Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="2e36a-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="2e36a-124">Lorsque vous définissez l’argument *OrderBy* , les enregistrements sont triés par défaut par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="2e36a-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="2e36a-125">Pour trier les enregistrements dans l’ordre décroissant, saisissez DESC à la fin de l’expression d’argument *OrderBy (TriPar)* .</span><span class="sxs-lookup"><span data-stu-id="2e36a-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="2e36a-126">Par exemple, pour trier les enregistrements clients dans l’ordre décroissant par contact, définissez l’argument *OrderBy* sur « ContactName DESC ».</span><span class="sxs-lookup"><span data-stu-id="2e36a-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="2e36a-127">Pour trier les noms par ordre décroissant de LastName et FirstName croissant, définissez l’argument *OrderBy* sur « LastName DESC, FirstName ASC ».</span><span class="sxs-lookup"><span data-stu-id="2e36a-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

