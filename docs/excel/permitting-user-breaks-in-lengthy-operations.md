---
title: Autorisation des interruptions utilisateur dans les opérations longues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007],concurrent tasks [Excel 2007],user breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414689"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="96dbb-104">Autorisation des interruptions utilisateur dans les opérations longues</span><span class="sxs-lookup"><span data-stu-id="96dbb-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="96dbb-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96dbb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="96dbb-106">Même si Windows utilise le multitâche préemptif, où l’exécution de vos fonctions ou commandes peut prendre beaucoup de temps, il est bon de donner un peu de temps au système d’exploitation de temps en temps pour l’aider à planifier des tâches simultanées.</span><span class="sxs-lookup"><span data-stu-id="96dbb-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="96dbb-107">À l’aide des appels Windows natifs, vous pouvez le faire à l’aide de la fonction de veille.</span><span class="sxs-lookup"><span data-stu-id="96dbb-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="96dbb-108">À l’aide de l’API C, vous pouvez le faire à l’aide de la fonction [xlAbort](xlabort.md), qui produit non seulement le processeur pendant un instant, mais vérifie également si l’utilisateur a appuy sur la touche d’annulation, **ÉCHAP**.</span><span class="sxs-lookup"><span data-stu-id="96dbb-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="96dbb-109">La **fonction xlAbort** permet donc à votre code de vérifier si l’utilisateur souhaite mettre fin au processus, d’y faire le nettoyage nécessaire, puis de renvoyer le contrôle à Excel.</span><span class="sxs-lookup"><span data-stu-id="96dbb-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="96dbb-110">La fonction vous permet également d’effacer la condition d’coupure.</span><span class="sxs-lookup"><span data-stu-id="96dbb-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="96dbb-111">Cela permet à vos commandes d’afficher une boîte de dialogue pour vérifier si l’utilisateur souhaite mettre fin à la commande.</span><span class="sxs-lookup"><span data-stu-id="96dbb-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="96dbb-112">Si l’utilisateur ne souhaite pas mettre fin à la commande, l’appel de la fonction **xlAbort** avec l’argument  *FALSE*  permet d’effacer la coupure.</span><span class="sxs-lookup"><span data-stu-id="96dbb-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="96dbb-113">(L’argument par défaut est  *TRUE,*  qui vérifie simplement la condition, mais ne l’effacera pas.)</span><span class="sxs-lookup"><span data-stu-id="96dbb-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="96dbb-114">Vous pouvez appeler la **fonction xlAbort** à partir d’une fonction définie par l’utilisateur (UDF) ou d’une commande XLL.</span><span class="sxs-lookup"><span data-stu-id="96dbb-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="96dbb-115">Dans une fonction UDF, lorsque la fonction **xlAbort** renvoie **true**, après avoir détecté un coupure utilisateur, vous avez généralement raccourci le calcul de la fonction et renvoyer une valeur pour indiquer que le calcul n’a pas été effectué, peut-être une erreur ou zéro.</span><span class="sxs-lookup"><span data-stu-id="96dbb-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="96dbb-116">Vous ne souhaitez pas effacer la condition de rupture afin que d’autres instances de fonctions longues qui vérifient également cette condition se cassent également.</span><span class="sxs-lookup"><span data-stu-id="96dbb-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="96dbb-117">Excel permet d’effacer implicitement cette condition à la fin d’un recalcul.</span><span class="sxs-lookup"><span data-stu-id="96dbb-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="96dbb-118">Lorsque vous détectez une condition d’coupure dans une commande, vous l’effacerez généralement en appelant à nouveau la fonction **xlAbort** avec l’argument **FALSE,** bien qu’Excel l’effacera implicitement à la fin d’une commande.</span><span class="sxs-lookup"><span data-stu-id="96dbb-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96dbb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96dbb-119">See also</span></span>



[<span data-ttu-id="96dbb-120">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="96dbb-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="96dbb-121">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="96dbb-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="96dbb-122">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="96dbb-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="96dbb-123">Accès à l’instance Excel et aux handles de fenêtre principaux</span><span class="sxs-lookup"><span data-stu-id="96dbb-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

