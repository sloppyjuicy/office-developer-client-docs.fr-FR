---
title: Autorisation utilisateur sauts dans les opérations de longue durée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonction xlAbort [excel 2007], tâches simultanées [Excel 2007], sauts utilisateur [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782181"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="af666-104">Autorisation utilisateur sauts dans les opérations de longue durée</span><span class="sxs-lookup"><span data-stu-id="af666-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="af666-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af666-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="af666-106">Même si Windows utilise multitâche préventif, où vos fonctions ou des commandes peuvent prendre beaucoup de temps d’exécution, il est conseillé de rendement peu de temps pour le système d’exploitation autre afin de planifier des tâches simultanées.</span><span class="sxs-lookup"><span data-stu-id="af666-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="af666-107">À l’aide des appels Windows natives, procéder à l’aide de la fonction de mise en veille.</span><span class="sxs-lookup"><span data-stu-id="af666-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="af666-108">À l’aide de l’API C, vous pouvez le faire à l’aide de la [fonction xlAbort](xlabort.md), non seulement génère le processeur pour une conversation instantanée, mais également vérifie si l’utilisateur a appuyé sur la touche Annuler, **ÉCHAP**.</span><span class="sxs-lookup"><span data-stu-id="af666-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="af666-109">La fonction **xlAbort** permet donc de votre code pour vérifier si l’utilisateur souhaite mettre fin au processus, de nettoyage nécessaires et rendre ensuite le contrôle vers Excel.</span><span class="sxs-lookup"><span data-stu-id="af666-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="af666-110">La fonction permet d’effacer la condition d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="af666-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="af666-111">Cela permet à vos commandes afficher une boîte de dialogue pour vérifier si l’utilisateur souhaite mettre fin à la commande.</span><span class="sxs-lookup"><span data-stu-id="af666-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="af666-112">Si l’utilisateur ne souhaite pas mettre fin à la commande, l’appel de la fonction **xlAbort** avec l’argument *FALSE* efface l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="af666-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="af666-113">(L’argument par défaut est *TRUE* , ce qui vérifie la condition simplement, mais ne la supprime pas).</span><span class="sxs-lookup"><span data-stu-id="af666-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="af666-114">Vous pouvez appeler la fonction **xlAbort** à partir d’une fonction définie par l’utilisateur (UDF) ou d’une commande XLL.</span><span class="sxs-lookup"><span data-stu-id="af666-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="af666-115">Dans un fichier UDF, lorsque la fonction **xlAbort** renvoie **la valeur TRUE**, avoir détecté un saut de l’utilisateur, vous généralement coupés le calcul de la fonction et renvoyer une valeur pour indiquer que le calcul n’a pas terminé, par exemple une erreur ou zéro.</span><span class="sxs-lookup"><span data-stu-id="af666-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="af666-116">Vous ne devez pas désactiver la condition d’arrêt afin que d’autres instances de fonctions longues qui également vérifient cette condition d’arrêt également.</span><span class="sxs-lookup"><span data-stu-id="af666-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="af666-117">Excel efface implicitement cette condition lorsque le recalcul se termine.</span><span class="sxs-lookup"><span data-stu-id="af666-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="af666-118">Lorsque vous détectez une condition d’arrêt dans une commande, vous désactivez généralement la condition en appelant la fonction **xlAbort** à l’aide de l’argument **FALSE**, bien qu’Excel efface implicitement cette condition issue d’une commande.</span><span class="sxs-lookup"><span data-stu-id="af666-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af666-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af666-119">See also</span></span>



[<span data-ttu-id="af666-120">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="af666-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="af666-121">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="af666-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="af666-122">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="af666-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="af666-123">Instance d’Excel Access et les poignées de la fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="af666-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

