---
title: Action de Macro ExécuterMacroDonnées (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Vous pouvez utiliser l’action ExécuterMacroDonnées pour exécuter une macro de données autonome.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781972"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="5a7c5-103">Action de Macro ExécuterMacroDonnées (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="5a7c5-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="5a7c5-104">Vous pouvez utiliser l’action **ExécuterMacroDonnées** pour exécuter une macro de données autonome.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5a7c5-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5a7c5-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5a7c5-107">Setting</span></span>

<span data-ttu-id="5a7c5-108">L'action **ExécuterMacroDonnées** utilise l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="5a7c5-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="5a7c5-109">**Action argument**</span></span>|<span data-ttu-id="5a7c5-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="5a7c5-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5a7c5-111">_Nom de la macro_</span><span class="sxs-lookup"><span data-stu-id="5a7c5-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="5a7c5-112">Nom de la macro de données à exécuter.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a7c5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5a7c5-113">Remarks</span></span>

<span data-ttu-id="5a7c5-114">Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="5a7c5-115">Si la macro de données nécessite des paramètres, les zones de texte apparaissent dans laquelle vous pouvez taper dans les arguments.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="5a7c5-p103">Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.</span><span class="sxs-lookup"><span data-stu-id="5a7c5-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

