---
title: Action de Macro ArrêtMacro
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3880b57e235520e3351ef16282fb8883d93b11e3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873711"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="46ca5-102">Action de Macro ArrêtMacro</span><span class="sxs-lookup"><span data-stu-id="46ca5-102">StopMacro Macro Action</span></span>

<span data-ttu-id="46ca5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46ca5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46ca5-104">Vous pouvez utiliser l’action **ArrêtMacro** pour arrêter la macro en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="46ca5-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="46ca5-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="46ca5-105">Setting</span></span>

<span data-ttu-id="46ca5-106">L’action **ArrêtMacro** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="46ca5-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ca5-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="46ca5-107">Remarks</span></span>

<span data-ttu-id="46ca5-108">Vous utilisez généralement cette action quand une condition rend nécessaire pour arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="46ca5-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="46ca5-109">Vous pouvez utiliser une expression conditionnelle dans la ligne d'action de la macro contenant cette action.</span><span class="sxs-lookup"><span data-stu-id="46ca5-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="46ca5-110">Lorsque l’expression a la valeur **True** (– 1), Microsoft Access arrête la macro.</span><span class="sxs-lookup"><span data-stu-id="46ca5-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="46ca5-111">Par exemple, vous pouvez créer une macro qui ouvre un formulaire affichant les totaux de la commande quotidienne pour la date entrée dans la boîte de dialogue personnalisée.</span><span class="sxs-lookup"><span data-stu-id="46ca5-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="46ca5-112">Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle de **Date de la commande** dans la boîte de dialogue contient une date valide.</span><span class="sxs-lookup"><span data-stu-id="46ca5-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="46ca5-113">Le cas contraire, l’action de **contrôle zonemessage** peut afficher un message d’erreur et l’action **ArrêtMacro** arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="46ca5-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="46ca5-114">Si la macro a utilisé les actions **écho** ou **avertissements** pour désactiver l’écho ou l’affichage des messages système, l’action **ArrêtMacro** automatiquement réactive les.</span><span class="sxs-lookup"><span data-stu-id="46ca5-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="46ca5-115">Cette action n'est pas disponible dans les modules Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="46ca5-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="46ca5-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ca5-116">Example</span></span>

<span data-ttu-id="46ca5-117">La macro suivante illustre l'utilisation de l'action **SurErreur**.</span><span class="sxs-lookup"><span data-stu-id="46ca5-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="46ca5-118">Dans cet exemple, l'action **SurErreur** spécifie qu'Access exécute une macro de gestion des erreurs personnalisée nommée GestionnaireErreur lorsqu'une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="46ca5-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="46ca5-119">Lorsqu’une erreur se produit, le submacro CatchErrors est appelée.</span><span class="sxs-lookup"><span data-stu-id="46ca5-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="46ca5-120">Si le numéro d’erreur est 2102, un message s’affiche et l’exécution de la macro est interrompue.</span><span class="sxs-lookup"><span data-stu-id="46ca5-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="46ca5-121">Sinon, un message décrivant l’erreur s’affiche et la macro est interrompue de sorte que vous pouvez effectuer des opérations de dépannage.</span><span class="sxs-lookup"><span data-stu-id="46ca5-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="46ca5-122">Cette macro affiche une zone de message qui fait référence à l'objet **MacroError** pour afficher des informations sur l'erreur.</span><span class="sxs-lookup"><span data-stu-id="46ca5-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="46ca5-123">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="46ca5-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
