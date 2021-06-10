---
title: SetReturnVar, action de macro
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308672"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="67482-102">SetReturnVar, action de macro</span><span class="sxs-lookup"><span data-stu-id="67482-102">SetReturnVar macro action</span></span>

<span data-ttu-id="67482-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67482-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67482-104">**L’action SetReturnVar** crée une variable de retour et la définit sur une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="67482-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="67482-105">**L’action SetReturnVar** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="67482-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="67482-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="67482-106">Setting</span></span>

<span data-ttu-id="67482-107">**L’action SetReturnVar** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="67482-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67482-108">Argument</span><span class="sxs-lookup"><span data-stu-id="67482-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="67482-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="67482-109">Required</span></span></p></th>
<th><p><span data-ttu-id="67482-110">Description</span><span class="sxs-lookup"><span data-stu-id="67482-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67482-111">Nom</span><span class="sxs-lookup"><span data-stu-id="67482-111">Name</span></span></p></td>
<td><p><span data-ttu-id="67482-112">Oui</span><span class="sxs-lookup"><span data-stu-id="67482-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="67482-113">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="67482-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67482-114">Expression</span><span class="sxs-lookup"><span data-stu-id="67482-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="67482-115">Oui</span><span class="sxs-lookup"><span data-stu-id="67482-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="67482-116">Expression destiné à être utilisé pour définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="67482-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="67482-117">Ne faites pas précéder l’expression d’un signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="67482-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="67482-118">Vous pouvez cliquer sur le bouton <strong>Générer</strong> afin d’utiliser le <strong>Générateur d’expressions</strong> pour définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="67482-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="67482-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="67482-119">Remarks</span></span>

<span data-ttu-id="67482-120">**L’action SetReturnVar** est utilisée pour créer une variable **ReturnVar**, qui peut être utilisée par les macros qui appellent une macro de données à l’aide de l’action **ExécuterMacroDonnées.**</span><span class="sxs-lookup"><span data-stu-id="67482-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="67482-121">Une fois **qu’unevar** de retour est créée par l’action **SetReturnVar,** la macro appelant peut l’utiliser dans une expression.</span><span class="sxs-lookup"><span data-stu-id="67482-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="67482-122">Par exemple, si vous avez créé une variable **ReturnVar** nommée **UpdateSuccess,** vous pouvez utiliser la variable à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="67482-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="67482-123">**L’action SetReturnVar** ne peut être utilisée que dans les macros de données nommées.</span><span class="sxs-lookup"><span data-stu-id="67482-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="67482-124">Elle n’est pas disponible dans les macros de données attachées à un événement de macro de données.</span><span class="sxs-lookup"><span data-stu-id="67482-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="67482-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="67482-125">Example</span></span>

<span data-ttu-id="67482-126">L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur à partir d’une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="67482-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="67482-127">Une valeur ReturnVar nommée **CurrentServiceRequest** est renvoyée à la macro ou à la sous-Visual Basic pour Applications (VBA) qui a appelé la macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="67482-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="67482-128">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="67482-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
