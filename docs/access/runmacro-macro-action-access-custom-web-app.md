---
title: ExécuterMacro, Action de Macro (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Vous pouvez utiliser l’action ExécuterMacro pour exécuter une macro de l’interface utilisateur.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781977"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="2f3f6-103">ExécuterMacro, Action de Macro (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2f3f6-104">Vous pouvez utiliser l’action **ExécuterMacro** pour exécuter une macro de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2f3f6-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2f3f6-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f3f6-107">Setting</span></span>

<span data-ttu-id="2f3f6-108">L'action **ExécuterMacro** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="2f3f6-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="2f3f6-109">**Action argument**</span></span>|<span data-ttu-id="2f3f6-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="2f3f6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f3f6-111">**Nom de la macro**</span><span class="sxs-lookup"><span data-stu-id="2f3f6-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="2f3f6-112">Nom de la macro d’interface utilisateur à exécuter.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f3f6-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f3f6-113">Remarks</span></span>

<span data-ttu-id="2f3f6-114">Lorsque vous exécutez une macro d’interface utilisateur contenant l’action **ExécuterMacro** et qu’elle atteint l’action **ExécuterMacro** , Access exécute la macro appelée de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="2f3f6-115">Lorsque la macro d’interface utilisateur appelée est terminée, Access retourne à la macro d’interface utilisateur d’origine et exécute l’action suivante.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

