---
title: Group, instruction de macro
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35f9ad1d445dbddaa5487e28da60b9202a72dae1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879850"
---
# <a name="group-macro-statement"></a><span data-ttu-id="14ff0-102">Group, instruction de macro</span><span class="sxs-lookup"><span data-stu-id="14ff0-102">Group Macro Statement</span></span>


<span data-ttu-id="14ff0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14ff0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14ff0-104">L’instruction **Group** vous permet de spécifier un bloc d’actions dans une macro que vous pouvez développer ou réduire.</span><span class="sxs-lookup"><span data-stu-id="14ff0-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="14ff0-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="14ff0-105">Setting</span></span>

<span data-ttu-id="14ff0-106">L'instruction **Group** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="14ff0-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14ff0-107">Argument</span><span class="sxs-lookup"><span data-stu-id="14ff0-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="14ff0-108">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="14ff0-108">Required</span></span></p></th>
<th><p><span data-ttu-id="14ff0-109">Description</span><span class="sxs-lookup"><span data-stu-id="14ff0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14ff0-110"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="14ff0-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="14ff0-111">Non</span><span class="sxs-lookup"><span data-stu-id="14ff0-111">No</span></span></p></td>
<td><p><span data-ttu-id="14ff0-112">Chaîne qui s’affiche comme titre d’un groupe lorsqu’il est réduit.</span><span class="sxs-lookup"><span data-stu-id="14ff0-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="14ff0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="14ff0-113">Remarks</span></span>

<span data-ttu-id="14ff0-p101">L'instruction **Group** ne définit pas une région d'une macro qui peut être exécutée séparément. Utilisez l'instruction **[Submacro](submacro-macro-statement.md)** pour définir un ensemble d'actions à exécuter séparément dans la fenêtre **Concepteur de macros**.</span><span class="sxs-lookup"><span data-stu-id="14ff0-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

