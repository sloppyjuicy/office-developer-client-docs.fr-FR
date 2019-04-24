---
title: DeleteRecord Data, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Vous pouvez utiliser l'action SupprimerEnregistrement pour supprimer un enregistrement.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282114"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="1dda1-103">DeleteRecord Data, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="1dda1-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="1dda1-104">Vous pouvez utiliser l'action **SupprimerEnregistrement** pour supprimer un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1dda1-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1dda1-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1dda1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1dda1-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1dda1-107">Setting</span></span>

<span data-ttu-id="1dda1-108">L'action **DeleteRecord** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="1dda1-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="1dda1-109">**Argument**</span><span class="sxs-lookup"><span data-stu-id="1dda1-109">**Argument**</span></span>|<span data-ttu-id="1dda1-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="1dda1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1dda1-111">**Alias d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="1dda1-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="1dda1-112">Chaîne qui identifie l’enregistrement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="1dda1-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="1dda1-113">Si l'argument *alias* n'est pas spécifié, l'enregistrement actif est supprimé.</span><span class="sxs-lookup"><span data-stu-id="1dda1-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dda1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1dda1-114">Remarks</span></span>

<span data-ttu-id="1dda1-115">Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1dda1-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="1dda1-116">Par exemple, utilisez la syntaxe suivante pour faire référence au dernier enregistrement créé:</span><span class="sxs-lookup"><span data-stu-id="1dda1-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


