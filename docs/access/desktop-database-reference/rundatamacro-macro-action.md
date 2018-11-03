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
ms.openlocfilehash: c1d540b909a2ac5741719470f5632e34205806ff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927983"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="dce78-102">RunDataMacro, action de macro</span><span class="sxs-lookup"><span data-stu-id="dce78-102">RunDataMacro macro action</span></span>

<span data-ttu-id="dce78-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dce78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dce78-104">Vous pouvez utiliser l'action **ExécuterMacroDonnées** pour exécuter une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="dce78-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="dce78-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dce78-105">Setting</span></span>

<span data-ttu-id="dce78-106">L'action **ExécuterMacroDonnées** utilise l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="dce78-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dce78-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="dce78-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dce78-108">Description</span><span class="sxs-lookup"><span data-stu-id="dce78-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dce78-109">Name</span><span class="sxs-lookup"><span data-stu-id="dce78-109">Name</span></span></p></td>
<td><p><span data-ttu-id="dce78-110">Nom de la macro de données à exécuter.</span><span class="sxs-lookup"><span data-stu-id="dce78-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dce78-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dce78-111">Remarks</span></span>

<span data-ttu-id="dce78-112">Vous pouvez utiliser l’action **ExécuterMacroDonnées** dans les macros, nommé macros de données et les événements de macros suivants : **[événement de macro après suppression](after-delete-macro-event.md)**, **[événement de macro après insertion](after-insert-macro-event.md)** et **[événement de macro après la mise à jour](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="dce78-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete macro event](after-delete-macro-event.md)**, **[After Insert macro event](after-insert-macro-event.md)** and **[After Update macro event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="dce78-113">Le nom de la macro de données doit inclure la table à laquelle elle est attachée (par exemple **Comments.AddComment**, pas seulement **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="dce78-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="dce78-114">Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres.</span><span class="sxs-lookup"><span data-stu-id="dce78-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="dce78-115">Si la macro de données nécessite des paramètres, les zones de texte apparaissent dans laquelle vous pouvez taper dans les arguments.</span><span class="sxs-lookup"><span data-stu-id="dce78-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="dce78-p102">Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.</span><span class="sxs-lookup"><span data-stu-id="dce78-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="dce78-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="dce78-118">Example</span></span>

<span data-ttu-id="dce78-119">L’exemple suivant montre comment passer un paramètre à une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="dce78-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="dce78-120">La macro de données dmGetCurrentServiceRequest de la table tblServiceRequests est appelée à l’aide de l’action ExécuterMacroDonnées.</span><span class="sxs-lookup"><span data-stu-id="dce78-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="dce78-121">Lorsque la dmGetCurrentServiceRequest est terminée, la variable CurrentServiceRequest renvoyé formulaire que la macro de données est écrit dans la zone de texte txtCurrentSR.</span><span class="sxs-lookup"><span data-stu-id="dce78-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="dce78-122">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="dce78-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
