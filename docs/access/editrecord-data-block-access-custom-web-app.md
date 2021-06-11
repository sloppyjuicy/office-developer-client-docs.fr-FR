---
title: EditRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Vous pouvez utiliser le bloc de données ModifierEnregistrement pour modifier les valeurs contenues dans un enregistrement existant.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418343"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="c6b3d-103">EditRecord Data Block (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="c6b3d-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="c6b3d-104">Vous pouvez utiliser le bloc de données **ModifierEnregistrement** pour modifier les valeurs contenues dans un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c6b3d-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6b3d-107">Le bloc de données **ModifierEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="c6b3d-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c6b3d-108">Setting</span></span>

<span data-ttu-id="c6b3d-109">Le bloc de données **ModifierEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="c6b3d-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="c6b3d-110">**Argument**</span></span>|<span data-ttu-id="c6b3d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c6b3d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6b3d-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c6b3d-112">**Alias**</span></span> <br/> |<span data-ttu-id="c6b3d-113">Chaîne qui identifie l’enregistrement à modifier.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="c6b3d-114">Si  *l’argument Alias*  n’est pas spécifié, l’enregistrement actuel est modifié.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6b3d-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6b3d-115">Remarks</span></span>

<span data-ttu-id="c6b3d-116">Après **l’instruction EditRecord,** vous pouvez insérer un bloc de commandes qui s’exécute avant que les modifications apportées à l’enregistrement soient enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="c6b3d-117">Les actions suivantes sont disponibles dans un bloc **de données EditRecord.**</span><span class="sxs-lookup"><span data-stu-id="c6b3d-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="c6b3d-118">Action de macro AnnulerModificationEnregistrement</span><span class="sxs-lookup"><span data-stu-id="c6b3d-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="c6b3d-119">Instruction de macro Comment</span><span class="sxs-lookup"><span data-stu-id="c6b3d-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="c6b3d-120">Instruction de macro Group</span><span class="sxs-lookup"><span data-stu-id="c6b3d-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="c6b3d-121">Instruction de macro If... Then... Else</span><span class="sxs-lookup"><span data-stu-id="c6b3d-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="c6b3d-122">Action de macro DéfinirChamp</span><span class="sxs-lookup"><span data-stu-id="c6b3d-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="c6b3d-123">Action de macro DéfinirVarLocale</span><span class="sxs-lookup"><span data-stu-id="c6b3d-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="c6b3d-124">Utilisez l'action **DéfinirChamp** pour spécifier les nouvelles valeurs d'un champ dans l'enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="c6b3d-125">Vous pouvez utiliser un **if... Ensuite... Instruction Else** pour effectuer des opérations basées sur une condition.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="c6b3d-p104">Pour annuler la modification d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **ModifierEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="c6b3d-128">Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c6b3d-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="c6b3d-129">Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement créé :</span><span class="sxs-lookup"><span data-stu-id="c6b3d-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


