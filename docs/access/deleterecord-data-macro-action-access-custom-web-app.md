---
title: Action de Macro de données SupprimerEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Vous pouvez utiliser l’action SupprimerEnregistrement pour supprimer un enregistrement.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781781"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="f06bb-103">Action de Macro de données SupprimerEnregistrement (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="f06bb-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="f06bb-104">Vous pouvez utiliser l'action **SupprimerEnregistrement** pour supprimer un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f06bb-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f06bb-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f06bb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f06bb-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="f06bb-107">Setting</span></span>

<span data-ttu-id="f06bb-108">L’action **SupprimerEnregistrement** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="f06bb-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="f06bb-109">**Argument**</span><span class="sxs-lookup"><span data-stu-id="f06bb-109">**Argument**</span></span>|<span data-ttu-id="f06bb-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="f06bb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f06bb-111">**Alias d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="f06bb-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="f06bb-112">Une chaîne qui identifie l’enregistrement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="f06bb-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="f06bb-113">Si l’argument *Alias* n’est pas spécifié, l’enregistrement actif est supprimé.</span><span class="sxs-lookup"><span data-stu-id="f06bb-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f06bb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f06bb-114">Remarks</span></span>

<span data-ttu-id="f06bb-115">Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="f06bb-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="f06bb-116">Par exemple, utilisez la syntaxe suivante pour faire référence à l’enregistrement plus récent :</span><span class="sxs-lookup"><span data-stu-id="f06bb-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


