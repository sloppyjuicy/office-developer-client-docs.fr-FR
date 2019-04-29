---
title: RequeryRecords, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Vous pouvez utiliser l'action RequeryRecords pour actualiser, trier et filtrer les données dans l'affichage actif en actualisant la source de la vue.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439246"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="80adb-103">RequeryRecords, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="80adb-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="80adb-104">Vous pouvez utiliser l'action **RequeryRecords** pour actualiser, trier et filtrer les données dans l'affichage actif en actualisant la source de la vue.</span><span class="sxs-lookup"><span data-stu-id="80adb-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="80adb-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="80adb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="80adb-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="80adb-107">Setting</span></span>

<span data-ttu-id="80adb-108">L'action **RequeryRecords** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="80adb-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="80adb-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="80adb-109">**Parameter**</span></span>|<span data-ttu-id="80adb-110">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="80adb-110">**Required**</span></span>|<span data-ttu-id="80adb-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="80adb-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80adb-112">**Où =**</span><span class="sxs-lookup"><span data-stu-id="80adb-112">**Where=**</span></span> <br/> |<span data-ttu-id="80adb-113">Non</span><span class="sxs-lookup"><span data-stu-id="80adb-113">No</span></span>  <br/> |<span data-ttu-id="80adb-114">Une clause SQL WHERE qui limite les enregistrements dans l'affichage.</span><span class="sxs-lookup"><span data-stu-id="80adb-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="80adb-115">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="80adb-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="80adb-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="80adb-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="80adb-117">Non</span><span class="sxs-lookup"><span data-stu-id="80adb-117">No</span></span>  <br/> |<span data-ttu-id="80adb-118">Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</span><span class="sxs-lookup"><span data-stu-id="80adb-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="80adb-119">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="80adb-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80adb-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="80adb-120">Remarks</span></span>

<span data-ttu-id="80adb-121">Tout tri ou filtrage appliqué par l'utilisateur est effacé lors de l'appel de l'action **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="80adb-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="80adb-122">L'argument *orderby* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="80adb-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="80adb-123">Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="80adb-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="80adb-124">Lorsque vous définissez l'argument *orderby* , les enregistrements sont triés par défaut dans l'ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="80adb-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="80adb-125">Pour trier les enregistrements par ordre décroissant, entrez DESC à la fin de l'expression de l'argument *orderby* .</span><span class="sxs-lookup"><span data-stu-id="80adb-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="80adb-126">Par exemple, pour trier les enregistrements clients par nom de contact dans l'ordre décroissant, définissez l'argument *orderby* sur «ContactName DESC».</span><span class="sxs-lookup"><span data-stu-id="80adb-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="80adb-127">Pour trier les noms par nom décroissant et par ordre croissant, définissez l'argument *orderby* sur «LastName DESC, FirstName ASC».</span><span class="sxs-lookup"><span data-stu-id="80adb-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

