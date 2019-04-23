---
title: OnError, action de macro
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288454"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="588b0-102">OnError, action de macro</span><span class="sxs-lookup"><span data-stu-id="588b0-102">OnError macro action</span></span>

<span data-ttu-id="588b0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="588b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="588b0-104">Utilisez l’action **SurErreur** pour indiquer ce qui doit se passer lorsqu’une erreur se produit dans une macro.</span><span class="sxs-lookup"><span data-stu-id="588b0-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="588b0-105">Setting</span><span class="sxs-lookup"><span data-stu-id="588b0-105">Setting</span></span>

<span data-ttu-id="588b0-106">L’action **SurErreur** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="588b0-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="588b0-107">Argument d’action</span><span class="sxs-lookup"><span data-stu-id="588b0-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="588b0-108">Description</span><span class="sxs-lookup"><span data-stu-id="588b0-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="588b0-109">Accédez à</span><span class="sxs-lookup"><span data-stu-id="588b0-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="588b0-p101">Spécifie le comportement général lorsqu’une erreur se produit. Cliquez sur la flèche déroulante, puis sur l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="588b0-p101">Specify the general behavior that should occur when an error is encountered. Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="588b0-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="588b0-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="588b0-113">Description</span><span class="sxs-lookup"><span data-stu-id="588b0-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="588b0-114"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="588b0-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="588b0-p102">Microsoft Office Access 2007 enregistre les détails de l’erreur dans l’objet <strong>MacroError</strong> mais n’arrête pas la macro. La macro passe à l’action suivante.</span><span class="sxs-lookup"><span data-stu-id="588b0-p102">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro. The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="588b0-117"><strong>Nom macro</strong></span><span class="sxs-lookup"><span data-stu-id="588b0-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="588b0-118">Access arrête l’exécution de la macro active et exécute la macro dont le nom figure dans l’argument <strong>Nom de la macro</strong>.</span><span class="sxs-lookup"><span data-stu-id="588b0-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="588b0-119"><strong>Fonctionner</strong></span><span class="sxs-lookup"><span data-stu-id="588b0-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="588b0-120">Access arrête l'exécution de la macro active et affiche un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="588b0-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="588b0-121">Nom macro</span><span class="sxs-lookup"><span data-stu-id="588b0-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="588b0-122">Si l'argument atteindre est défini sur nom de la macro, tapez le nom de la macro à utiliser pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="588b0-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="588b0-123">Le nom que vous tapez doit correspondre à un nom dans la colonne nom de la <strong>macro</strong> de la macro active; vous ne pouvez pas entrer le nom d'un autre objet de macro.</span><span class="sxs-lookup"><span data-stu-id="588b0-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="588b0-124">Dans l'exemple ci-dessous, la macro <strong>ErrorHandler</strong> est contenue dans le même objet macro que l'action SurErreur. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="588b0-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="588b0-125">Cet argument doit rester vide si l’argument Atteindre est défini sur <strong>Suivant</strong> ou sur <strong>Échec</strong>.</span><span class="sxs-lookup"><span data-stu-id="588b0-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="588b0-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="588b0-126">Remarks</span></span>

- <span data-ttu-id="588b0-p104">L’action **SurErreur** est généralement placée au début d’une macro, mais vous pouvez également la placer plus loin dans la macro. Les règles établies par cette action prendront effet dès exécution de l’action.</span><span class="sxs-lookup"><span data-stu-id="588b0-p104">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro. The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="588b0-129">Si vous définissez l'argument Atteindre sur **Échec**, Access se comporte de la même manière que si la macro ne contenait pas d'action **SurErreur**.</span><span class="sxs-lookup"><span data-stu-id="588b0-129">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro.</span></span> <span data-ttu-id="588b0-130">Autrement dit, si une erreur se produit, Access arrête la macro et affiche un message d'erreur standard.</span><span class="sxs-lookup"><span data-stu-id="588b0-130">That is, if an error is encountered, Access stops the macro and displays a standard error message.</span></span> <span data-ttu-id="588b0-131">Le paramètre **Échec** est principalement utilisé pour désactiver la gestion des erreurs établie précédemment dans une macro.</span><span class="sxs-lookup"><span data-stu-id="588b0-131">The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="588b0-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="588b0-132">Example</span></span>

<span data-ttu-id="588b0-133">La macro suivante illustre l'utilisation de l'action **SurErreur**.</span><span class="sxs-lookup"><span data-stu-id="588b0-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="588b0-134">Dans cet exemple, l'action **SurErreur** spécifie qu'Access exécute une macro de gestion des erreurs personnalisée nommée GestionnaireErreur lorsqu'une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="588b0-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="588b0-135">Lorsqu'une erreur se produit, la sous-macro CatchErrors est appelée.</span><span class="sxs-lookup"><span data-stu-id="588b0-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="588b0-136">Si le numéro de l'erreur est 2102, un message spécifique s'affiche et l'exécution de la macro est interrompue.</span><span class="sxs-lookup"><span data-stu-id="588b0-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="588b0-137">Dans le cas contraire, un message décrivant l'erreur s'affiche et la macro est suspendue pour vous permettre d'effectuer des procédures de dépannage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="588b0-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="588b0-138">Cette macro affiche une zone de message qui fait référence à l'objet **MacroError** pour afficher des informations sur l'erreur.</span><span class="sxs-lookup"><span data-stu-id="588b0-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="588b0-139">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="588b0-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
