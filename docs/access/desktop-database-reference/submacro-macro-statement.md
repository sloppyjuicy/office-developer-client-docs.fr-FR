---
title: Submacro, instruction de macro
TOCTitle: Submacro Macro Statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 822875db1cab865ce508b75673539b6c4a426917
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470305"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="f6b82-102">Submacro, instruction de macro</span><span class="sxs-lookup"><span data-stu-id="f6b82-102">Submacro Macro Statement</span></span>

<span data-ttu-id="f6b82-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6b82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f6b82-104">L'instruction **Submacro** définit une macro distincte dans la fenêtre Concepteur de macros.</span><span class="sxs-lookup"><span data-stu-id="f6b82-104">The **Submacro** statement defines a seperate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="f6b82-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f6b82-105">Setting</span></span>

<span data-ttu-id="f6b82-106">L'instruction **Submacro** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="f6b82-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6b82-107">Argument</span><span class="sxs-lookup"><span data-stu-id="f6b82-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="f6b82-108">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f6b82-108">Required</span></span></p></th>
<th><p><span data-ttu-id="f6b82-109">Description</span><span class="sxs-lookup"><span data-stu-id="f6b82-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6b82-110">Name</span><span class="sxs-lookup"><span data-stu-id="f6b82-110">Name</span></span></p></td>
<td><p><span data-ttu-id="f6b82-111">Oui</span><span class="sxs-lookup"><span data-stu-id="f6b82-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="f6b82-112">Chaîne qui apparaît comme nom de la macro.</span><span class="sxs-lookup"><span data-stu-id="f6b82-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="f6b82-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6b82-113">Example</span></span>

<span data-ttu-id="f6b82-114">La macro suivante illustre l'utilisation de l'action **SurErreur**.</span><span class="sxs-lookup"><span data-stu-id="f6b82-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="f6b82-115">Dans cet exemple, l'action **SurErreur** spécifie qu'Access exécute une macro de gestion des erreurs personnalisée nommée GestionnaireErreur lorsqu'une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="f6b82-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="f6b82-116">Lorsqu’une erreur se produit, le submacro CatchErrors est appelée.</span><span class="sxs-lookup"><span data-stu-id="f6b82-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="f6b82-117">Si le numéro d’erreur est 2102, un message s’affiche et l’exécution de la macro est interrompue.</span><span class="sxs-lookup"><span data-stu-id="f6b82-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="f6b82-118">Sinon, un message décrivant l’erreur s’affiche et la macro est interrompue de sorte que vous pouvez effectuer des opérations de dépannage.</span><span class="sxs-lookup"><span data-stu-id="f6b82-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="f6b82-119">Cette macro affiche une zone de message qui fait référence à l'objet **MacroError** pour afficher des informations sur l'erreur.</span><span class="sxs-lookup"><span data-stu-id="f6b82-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="f6b82-120">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f6b82-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
