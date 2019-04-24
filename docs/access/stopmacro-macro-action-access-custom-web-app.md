---
title: ArrêtMacro, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Vous pouvez utiliser l'action ArrêtMacro pour arrêter la macro en cours d'exécution.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311017"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="d5ccc-103">ArrêtMacro, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="d5ccc-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d5ccc-104">Vous pouvez utiliser l'action **ArrêtMacro** pour arrêter la macro en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d5ccc-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d5ccc-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d5ccc-107">Setting</span></span>

<span data-ttu-id="d5ccc-108">L'action **ArrêtMacro** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d5ccc-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5ccc-109">Remarks</span></span>

<span data-ttu-id="d5ccc-110">Cette action est généralement utilisée lorsqu'une condition nécessite l'arrêt de la macro.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="d5ccc-111">Par exemple, vous pouvez créer une macro d'interface utilisateur qui ouvre une vue illustrant le nombre total quotidien de commandes pour la date entrée dans l'affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="d5ccc-112">Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle Date commande dans la boîte de dialogue contient une date valide.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="d5ccc-113">Si ce n'est pas le cas, l'action **MessageBox** peut afficher un message d'erreur et l'action **ArrêtMacro** peut arrêter la macro de l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5ccc-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

