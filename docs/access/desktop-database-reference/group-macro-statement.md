---
title: Group, instruction de macro
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c82169ac430496587c6ebab5e439d70bc9319b5e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930888"
---
# <a name="group-macro-statement"></a><span data-ttu-id="34b9e-102">Group, instruction de macro</span><span class="sxs-lookup"><span data-stu-id="34b9e-102">Group macro statement</span></span>


<span data-ttu-id="34b9e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34b9e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34b9e-104">L’instruction **Group** vous permet de spécifier un bloc d’actions dans une macro que vous pouvez développer ou réduire.</span><span class="sxs-lookup"><span data-stu-id="34b9e-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="34b9e-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="34b9e-105">Setting</span></span>

<span data-ttu-id="34b9e-106">L'instruction **Group** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="34b9e-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34b9e-107">Argument</span><span class="sxs-lookup"><span data-stu-id="34b9e-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="34b9e-108">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="34b9e-108">Required</span></span></p></th>
<th><p><span data-ttu-id="34b9e-109">Description</span><span class="sxs-lookup"><span data-stu-id="34b9e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34b9e-110"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="34b9e-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="34b9e-111">Non</span><span class="sxs-lookup"><span data-stu-id="34b9e-111">No</span></span></p></td>
<td><p><span data-ttu-id="34b9e-112">Chaîne qui s’affiche comme titre d’un groupe lorsqu’il est réduit.</span><span class="sxs-lookup"><span data-stu-id="34b9e-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="34b9e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="34b9e-113">Remarks</span></span>

<span data-ttu-id="34b9e-p101">L'instruction **Group** ne définit pas une région d'une macro qui peut être exécutée séparément. Utilisez l'instruction **[Submacro](submacro-macro-statement.md)** pour définir un ensemble d'actions à exécuter séparément dans la fenêtre **Concepteur de macros**.</span><span class="sxs-lookup"><span data-stu-id="34b9e-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

