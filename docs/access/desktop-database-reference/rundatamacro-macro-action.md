---
title: RunDataMacro, action de macro
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306810"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="8a216-102">RunDataMacro, action de macro</span><span class="sxs-lookup"><span data-stu-id="8a216-102">RunDataMacro macro action</span></span>

<span data-ttu-id="8a216-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a216-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a216-104">Vous pouvez utiliser l’action **ExécuterMacroDonnées** pour exécuter une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="8a216-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="8a216-105">Setting</span><span class="sxs-lookup"><span data-stu-id="8a216-105">Setting</span></span>

<span data-ttu-id="8a216-106">L’action **ExécuterMacroDonnées** utilise l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="8a216-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a216-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="8a216-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8a216-108">Description</span><span class="sxs-lookup"><span data-stu-id="8a216-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a216-109">Nom</span><span class="sxs-lookup"><span data-stu-id="8a216-109">Name</span></span></p></td>
<td><p><span data-ttu-id="8a216-110">Nom de la macro de données à exécuter.</span><span class="sxs-lookup"><span data-stu-id="8a216-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8a216-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a216-111">Remarks</span></span>

<span data-ttu-id="8a216-112">Vous pouvez utiliser l’action **ExécuterMacroDonnées** dans les macros, les macros de données nommées et les événements de macro suivants : Événement de **[macro](after-delete-macro-event.md)** Après **[Suppression,](after-insert-macro-event.md)** Après Insertion et Événement de macro Après Mise à **[jour.](after-update-macro-event.md)**</span><span class="sxs-lookup"><span data-stu-id="8a216-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete macro event](after-delete-macro-event.md)**, **[After Insert macro event](after-insert-macro-event.md)** and **[After Update macro event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="8a216-113">Le nom de la macro de données doit inclure la table à laquelle elle est attachée (par exemple, **Comments.AddComment**, et pas seulement **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="8a216-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="8a216-114">Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8a216-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="8a216-115">Si la macro de données requiert des paramètres, les zones de texte s’affichent là où vous pouvez taper les arguments.</span><span class="sxs-lookup"><span data-stu-id="8a216-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="8a216-p102">Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.</span><span class="sxs-lookup"><span data-stu-id="8a216-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="8a216-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="8a216-118">Example</span></span>

<span data-ttu-id="8a216-119">L’exemple suivant montre comment passer un paramètre à une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="8a216-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="8a216-120">La macro de données dmGetCurrentServiceRequest de la table tblServiceRequests est appelée à l’aide de l’action ExécuterMacroDonnées.</span><span class="sxs-lookup"><span data-stu-id="8a216-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="8a216-121">Lorsque l’examen dmGetCurrentServiceRequest est terminé, la variable CurrentServiceRequest retourne le formulaire dans la zone de texte txtCurrentSR.</span><span class="sxs-lookup"><span data-stu-id="8a216-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="8a216-122">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8a216-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
