---
title: StopAllMacros, action de macro
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314475"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="a3f40-102">StopAllMacros, action de macro</span><span class="sxs-lookup"><span data-stu-id="a3f40-102">StopAllMacros macro action</span></span>


<span data-ttu-id="a3f40-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3f40-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3f40-104">L’action **ArrêtToutesMacros** permet d’arrêter toutes les macros en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a3f40-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="a3f40-105">Setting</span><span class="sxs-lookup"><span data-stu-id="a3f40-105">Setting</span></span>

<span data-ttu-id="a3f40-106">L’action **ArrêtToutesMacros** n’utilise aucun argument.</span><span class="sxs-lookup"><span data-stu-id="a3f40-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f40-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3f40-107">Remarks</span></span>

<span data-ttu-id="a3f40-p101">Cette action est généralement utilisée lorsqu’une condition d’erreur nécessite l’arrêt de toutes les macros. Vous pouvez utiliser une expression conditionnelle dans la ligne d’action de la macro contenant cette action. Lorsque l’expression renvoie la valeur **True** (–1), Microsoft Access arrête l’exécution de toutes les macros.</span><span class="sxs-lookup"><span data-stu-id="a3f40-p101">You typically use this action when an error condition makes it necessary to stop all macros. You can use a conditional expression in the macro's action row that contains this action. When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="a3f40-p102">C'est le cas, par exemple, lorsque l'affichage d'une boîte de message constitue l'une des actions complexes d'une macro, parmi lesquelles l'exécution d'autres macros. Si l'utilisateur clique sur **Annuler** dans cette boîte de message, l'action **ArrêtToutesMacros** peut entraîner l'arrêt de toutes les macros en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="a3f40-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="a3f40-113">Si les actions **Écho** ou **Avertissements** ont été utilisées par une macro pour désactiver un écho ou l'affichage des messages système, l'action **ArrêtToutesMacros** les réactivera automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a3f40-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="a3f40-114">Cette action n'est pas disponible dans les modules Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="a3f40-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

