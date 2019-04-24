---
title: RunDataMacro, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Vous pouvez utiliser l'action RunDataMacro pour exécuter une macro de données autonome.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304241"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="884dc-103">RunDataMacro, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="884dc-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="884dc-104">Vous pouvez utiliser l'action **RunDataMacro** pour exécuter une macro de données autonome.</span><span class="sxs-lookup"><span data-stu-id="884dc-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="884dc-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="884dc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="884dc-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="884dc-107">Setting</span></span>

<span data-ttu-id="884dc-108">L’action **ExécuterMacroDonnées** utilise l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="884dc-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="884dc-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="884dc-109">**Action argument**</span></span>|<span data-ttu-id="884dc-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="884dc-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="884dc-111">_Nom macro_</span><span class="sxs-lookup"><span data-stu-id="884dc-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="884dc-112">Nom de la macro de données à exécuter.</span><span class="sxs-lookup"><span data-stu-id="884dc-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="884dc-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="884dc-113">Remarks</span></span>

<span data-ttu-id="884dc-114">Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres.</span><span class="sxs-lookup"><span data-stu-id="884dc-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="884dc-115">Si la macro de données nécessite des paramètres, des zones de texte s'affichent à l'endroit où vous pouvez taper les arguments.</span><span class="sxs-lookup"><span data-stu-id="884dc-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="884dc-p103">Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.</span><span class="sxs-lookup"><span data-stu-id="884dc-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

