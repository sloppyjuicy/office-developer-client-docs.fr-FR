---
title: SetReturnVar Macro Action
TOCTitle: SetReturnVar Macro Action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa4380904888194bf1d954ebf5619cab7d155047
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470253"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="69dbc-102">SetReturnVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="69dbc-102">SetReturnVar Macro Action</span></span>

<span data-ttu-id="69dbc-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="69dbc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="69dbc-104">L’action **SetReturnVar** crée une variable de renvoi et lui affecte une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="69dbc-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="69dbc-105">L’action **SetReturnVar** est disponible uniquement dans les Macros de données.</span><span class="sxs-lookup"><span data-stu-id="69dbc-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="69dbc-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="69dbc-106">Setting</span></span>

<span data-ttu-id="69dbc-107">L’action **SetReturnVar** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="69dbc-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69dbc-108">Argument</span><span class="sxs-lookup"><span data-stu-id="69dbc-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="69dbc-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="69dbc-109">Required</span></span></p></th>
<th><p><span data-ttu-id="69dbc-110">Description</span><span class="sxs-lookup"><span data-stu-id="69dbc-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69dbc-111">Name</span><span class="sxs-lookup"><span data-stu-id="69dbc-111">Name</span></span></p></td>
<td><p><span data-ttu-id="69dbc-112">Oui</span><span class="sxs-lookup"><span data-stu-id="69dbc-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="69dbc-113">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="69dbc-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69dbc-114">Expression</span><span class="sxs-lookup"><span data-stu-id="69dbc-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="69dbc-115">Oui</span><span class="sxs-lookup"><span data-stu-id="69dbc-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="69dbc-116">Une expression qui sera utilisée pour définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="69dbc-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="69dbc-117">Ne faites pas précéder l’expression avec le signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="69dbc-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="69dbc-118">Vous pouvez cliquer sur le bouton <strong>Générer</strong> pour utiliser le <strong>Générateur d’Expression</strong> pour définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="69dbc-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="69dbc-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="69dbc-119">Remarks</span></span>

<span data-ttu-id="69dbc-120">L’action **SetReturnVar** est utilisée pour créer un **ReturnVar**, qui est la variable peut être utilisé par des macros qui appeler une macro de données à l’aide de l’action **ExécuterMacroDonnées** .</span><span class="sxs-lookup"><span data-stu-id="69dbc-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="69dbc-121">Une fois qu’un **ReturnVar** est créé par l’action **SetReturnVar** , la macro appelante peut l’utiliser dans une expression.</span><span class="sxs-lookup"><span data-stu-id="69dbc-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="69dbc-122">Par exemple, si vous avez créé un **ReturnVar** nommé **UpdateSuccess**, vous pouvez utiliser la variable à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="69dbc-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="69dbc-123">L’action **SetReturnVar** peut être utilisée uniquement dans les macros de données nommée.</span><span class="sxs-lookup"><span data-stu-id="69dbc-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="69dbc-124">Il n’est pas disponible dans les macros de données associées à un événement de macro de données.</span><span class="sxs-lookup"><span data-stu-id="69dbc-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="69dbc-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="69dbc-125">Example</span></span>

<span data-ttu-id="69dbc-126">L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur d’une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="69dbc-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="69dbc-127">Un ReturnVar nommé **CurrentServiceRequest** est renvoyé à la macro ou de Visual Basic pour sous-routine Applications (VBA) qui a appelé la macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="69dbc-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="69dbc-128">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="69dbc-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
