---
title: ExécuterMacroDonnées, action de macro
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9790faf03ba0f6ea02520abb525c4301ac2181e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469557"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="d61d0-102">ExécuterMacroDonnées, action de macro</span><span class="sxs-lookup"><span data-stu-id="d61d0-102">RunDataMacro Macro Action</span></span>

<span data-ttu-id="d61d0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d61d0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d61d0-104">Vous pouvez utiliser l'action **ExécuterMacroDonnées** pour exécuter une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="d61d0-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="d61d0-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d61d0-105">Setting</span></span>

<span data-ttu-id="d61d0-106">L'action **ExécuterMacroDonnées** utilise l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="d61d0-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d61d0-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d61d0-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d61d0-108">Description</span><span class="sxs-lookup"><span data-stu-id="d61d0-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d61d0-109">Name</span><span class="sxs-lookup"><span data-stu-id="d61d0-109">Name</span></span></p></td>
<td><p><span data-ttu-id="d61d0-110">Nom de la macro de données à exécuter.</span><span class="sxs-lookup"><span data-stu-id="d61d0-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d61d0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d61d0-111">Remarks</span></span>

<span data-ttu-id="d61d0-112">Vous pouvez utiliser l'action **ExécuterMacroDonnées** dans des macros, des macros de données nommées et les événements de macros suivants : **[Événement de macro Après suppression](after-delete-macro-event.md)**, **[Événement de macro Après insertion](after-insert-macro-event.md)** et **[Événement de macro Après MAJ](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="d61d0-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete Macro Event](after-delete-macro-event.md)**, **[After Insert Macro Event](after-insert-macro-event.md)** and **[After Update Macro Event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="d61d0-113">Le nom de la macro de données doit inclure la table à laquelle elle est attachée (par exemple **Comments.AddComment**, pas seulement **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="d61d0-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="d61d0-114">Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres.</span><span class="sxs-lookup"><span data-stu-id="d61d0-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="d61d0-115">Si la macro de données nécessite des paramètres, les zones de texte apparaissent dans laquelle vous pouvez taper dans les arguments.</span><span class="sxs-lookup"><span data-stu-id="d61d0-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="d61d0-p102">Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.</span><span class="sxs-lookup"><span data-stu-id="d61d0-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="d61d0-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="d61d0-118">Example</span></span>

<span data-ttu-id="d61d0-119">L’exemple suivant montre comment passer un paramètre à une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="d61d0-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="d61d0-120">La macro de données dmGetCurrentServiceRequest de la table tblServiceRequests est appelée à l’aide de l’action ExécuterMacroDonnées.</span><span class="sxs-lookup"><span data-stu-id="d61d0-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="d61d0-121">Lorsque la dmGetCurrentServiceRequest est terminée, la variable CurrentServiceRequest renvoyé formulaire que la macro de données est écrit dans la zone de texte txtCurrentSR.</span><span class="sxs-lookup"><span data-stu-id="d61d0-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="d61d0-122">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d61d0-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
