---
title: Bloc de données CréerEnregistrement (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Vous pouvez utiliser le bloc de données CréerEnregistrement pour créer un nouvel enregistrement dans la table spécifiée.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421374"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="bd6f3-103">Bloc de données CréerEnregistrement (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="bd6f3-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="bd6f3-104">Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="bd6f3-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bd6f3-107">Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="bd6f3-108">Setting</span><span class="sxs-lookup"><span data-stu-id="bd6f3-108">Setting</span></span>

<span data-ttu-id="bd6f3-109">Le bloc de données **CréerEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="bd6f3-110">Le bloc de données **CréerEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="bd6f3-111">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="bd6f3-111">**Argument name**</span></span>|<span data-ttu-id="bd6f3-112">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="bd6f3-112">**Required**</span></span>|<span data-ttu-id="bd6f3-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd6f3-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd6f3-114">**Créer un enregistrement dans**</span><span class="sxs-lookup"><span data-stu-id="bd6f3-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="bd6f3-115">Oui</span><span class="sxs-lookup"><span data-stu-id="bd6f3-115">Yes</span></span>  <br/> |<span data-ttu-id="bd6f3-116">Nom de la table dans laquelle créer le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="bd6f3-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="bd6f3-117">**Alias**</span></span> <br/> |<span data-ttu-id="bd6f3-118">Non</span><span class="sxs-lookup"><span data-stu-id="bd6f3-118">No</span></span>  <br/> |<span data-ttu-id="bd6f3-119">Chaîne qui identifie l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-119">A string that identifies the record.</span></span> <span data-ttu-id="bd6f3-120">Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-120">You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd6f3-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd6f3-121">Remarks</span></span>

<span data-ttu-id="bd6f3-122">L’enregistrement créé par \*\*CréerEnregistrement \*\* devient automatiquement l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="bd6f3-123">Après l'instruction **CréerEnregistrement** , vous pouvez insérer un bloc de commandes qui s'exécutera avant la validation du nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-123">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="bd6f3-124">Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-124">The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="bd6f3-125">Action de macro AnnulerModificationEnregistrement</span><span class="sxs-lookup"><span data-stu-id="bd6f3-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bd6f3-126">Instruction de macro Comment</span><span class="sxs-lookup"><span data-stu-id="bd6f3-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bd6f3-127">Instruction de macro Group</span><span class="sxs-lookup"><span data-stu-id="bd6f3-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bd6f3-128">Instruction de macro If... Then... Else</span><span class="sxs-lookup"><span data-stu-id="bd6f3-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bd6f3-129">Action de macro DéfinirChamp</span><span class="sxs-lookup"><span data-stu-id="bd6f3-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bd6f3-130">Action de macro DéfinirVarLocale</span><span class="sxs-lookup"><span data-stu-id="bd6f3-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="bd6f3-131">Après que l’action **CréerEnregistrement** a créé un enregistrement, utilisez l’action **DéfinirChamp** pour spécifier une valeur d’un champ dans le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="bd6f3-132">Vous pouvez utiliser une **If... Then... Else** pour effectuer des opérations en fonction d'une condition.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="bd6f3-p104">Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-p104">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="bd6f3-135">Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-135">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="bd6f3-136">Par exemple, utilisez la syntaxe suivante pour faire référence au champ AffectéÀ du dernier enregistrement créé.</span><span class="sxs-lookup"><span data-stu-id="bd6f3-136">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


