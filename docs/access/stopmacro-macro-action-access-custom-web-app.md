---
title: Action de Macro ArrêtMacro (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Vous pouvez utiliser l’action ArrêtMacro pour arrêter la macro en cours d’exécution.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781983"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="3b864-103">Action de Macro ArrêtMacro (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="3b864-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="3b864-104">Vous pouvez utiliser l’action **ArrêtMacro** pour arrêter la macro en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3b864-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3b864-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="3b864-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="3b864-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b864-107">Setting</span></span>

<span data-ttu-id="3b864-108">L’action **ArrêtMacro** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="3b864-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b864-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b864-109">Remarks</span></span>

<span data-ttu-id="3b864-110">Vous utilisez généralement cette action quand une condition rend nécessaire pour arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="3b864-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="3b864-111">Par exemple, vous pouvez créer une macro de l’interface utilisateur qui ouvre une vue affichant les totaux de la commande tous les jours à la date entrée dans la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="3b864-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="3b864-112">Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle de Date de la commande dans la boîte de dialogue contient une date valide.</span><span class="sxs-lookup"><span data-stu-id="3b864-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="3b864-113">Le cas contraire, l’action de **contrôle zonemessage** peut afficher un message d’erreur et l’action **ArrêtMacro** arrêter la macro d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3b864-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

