---
title: SingleStep, action de macro
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e934b290472dc4bb0ad8619b2ada6992b4215c0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726273"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="5de80-102">SingleStep, action de macro</span><span class="sxs-lookup"><span data-stu-id="5de80-102">SingleStep macro action</span></span>

<span data-ttu-id="5de80-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5de80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5de80-104">L'action **PasAPas** permet d'interrompre l'exécution d'une macro et d'ouvrir la boîte de dialogue **Pas à pas**.</span><span class="sxs-lookup"><span data-stu-id="5de80-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="5de80-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="5de80-105">Setting</span></span>

<span data-ttu-id="5de80-106">L'action **PasAPas** n'utilise aucun argument.</span><span class="sxs-lookup"><span data-stu-id="5de80-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de80-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5de80-107">Remarks</span></span>

- <span data-ttu-id="5de80-p101">L'action **PasAPas** permet de résoudre les dysfonctionnements d'une macro. Vous pouvez ajouter l'action **PasAPas** à une macro juste avant l'exécution d'une action que vous suspectez d'être la cause du problème. L'action interrompt l'exécution de la macro et ouvre la boîte de dialogue **Pas à pas**. Cette boîte de dialogue affiche les informations associées à l'action de la macro active, telles que le nom de la macro, les conditions spécifiées, le nom de l'action, les arguments et, le cas échéant, le numéro de l'erreur. Dans la boîte de dialogue, cliquez sur **Pas à pas** pour atteindre la prochaine action de macro, **Arrêter toutes les macros**, pour interrompre la macro active et, le cas échéant, les autres macros en cours d'exécution, ou cliquez sur **Continuer** pour arrêter la méthode Pas à pas et revenir à l'exécution normale de la macro.</span><span class="sxs-lookup"><span data-stu-id="5de80-p101">Use the **SingleStep** action to troubleshoot a macro that is not working properly. You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem. The action pauses the macro and opens the **Macro Single Step** dialog box. This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable. In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="5de80-p102">Utiliser l'action **PasAPas** équivaut à cliquer sur **Pas à pas** dans le groupe **Outils** de l'onglet **Créer** du Générateur de macro. La différence entre ce mode et l'exécution de l'action **PasAPas** est la suivante : en exécutant l'action, vous pouvez placer celle-ci dans la macro, à l'endroit précis où vous souhaitez démarrer le mode Pas à pas. Cette méthode vous évite de devoir passer en revue les actions précédentes avant d'accéder à celle que vous souhaitez examiner. En revanche, lorsque vous cliquez sur **Pas à pas** dans le Générateur de macro, vous devez le faire avant l'exécution de la macro. Dans ce cas, le mode Pas à pas démarre au niveau de la première action dans la macro.</span><span class="sxs-lookup"><span data-stu-id="5de80-p102">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder. The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin. That way, you don't have to step through all the previous actions to get to the one you want to examine. On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro. In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="5de80-p103">[!REMARQUE] Si vous utilisez le mode pas à pas jusqu'à la fin d'une macro, sans cliquer sur **Continuer**, ce mode restera actif jusqu'à la fin de l'exécution de la macro. Les éventuelles macros suivantes seront également exécutées en mode Pas à pas. Pour désactiver le mode Pas à pas, cliquez sur **Continuer** dans la boîte de dialogue **Pas à pas** ou, dans une macro ouverte en mode Création, cliquez sur **Pas à pas** dans le groupe **Outils** de l'onglet **Créer** pour annuler la sélection.</span><span class="sxs-lookup"><span data-stu-id="5de80-p103">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends. Any subsequent macro you run will start in single step mode. To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>
