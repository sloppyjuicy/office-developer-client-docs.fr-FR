---
title: RunMacro Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Vous pouvez utiliser l’action ExécuterMacro pour exécuter une macro d’interface utilisateur.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438441"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="7e8ef-103">RunMacro Macro Action (Application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="7e8ef-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="7e8ef-104">Vous pouvez utiliser l’action **ExécuterMacro** pour exécuter une macro d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7e8ef-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7e8ef-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7e8ef-107">Setting</span></span>

<span data-ttu-id="7e8ef-108">L’action **ExécuterMacro** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="7e8ef-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="7e8ef-109">**Action argument**</span></span>|<span data-ttu-id="7e8ef-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e8ef-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e8ef-111">**Nom macro**</span><span class="sxs-lookup"><span data-stu-id="7e8ef-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="7e8ef-112">Nom de la macro d’interface utilisateur à exécuter.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e8ef-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e8ef-113">Remarks</span></span>

<span data-ttu-id="7e8ef-114">Lorsque vous exécutez une macro d’interface utilisateur contenant l’action **ExécuterMacro** et qu’elle atteint l’action **ExécuterMacro,** Access exécute la macro d’interface utilisateur appelée.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="7e8ef-115">Lorsque la macro d’interface utilisateur appelée est terminée, Access revient à la macro d’interface utilisateur d’origine et exécute l’action suivante.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

