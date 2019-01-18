---
title: Exécuter une règle sur un ordinateur local
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9840133b7cd70b72e0bedf57931dfa9e53c67b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709935"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="ff91f-102">Exécuter une règle sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="ff91f-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="ff91f-103">Cet exemple montre comment exécuter une règle sur un ordinateur local à l’aide de la propriété [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) de l’objet [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ff91f-103">This example shows how to execute a rule on a local computer by using the [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="ff91f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff91f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ff91f-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ff91f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ff91f-p101">Si votre boîte aux lettres est hébergée sur un serveur Exchange, une règle est exécutable sur le serveur Exchange ou sur le client Outlook. Si la règle est exécutée sur le serveur, il n'est pas nécessaire qu'Outlook s'exécute pour que les conditions de la règle soient évaluées et que les actions de la règle soient exécutées. Si la règle est exécutée sur le client, Outlook doit s'exécuter pour que la règle s'exécute. Si la propriété [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) de l'objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) retourne **true**, la règle est exécutée sur le client.</span><span class="sxs-lookup"><span data-stu-id="ff91f-p101">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client. If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed. If the rule is executed on the client, Outlook must be running for the rule to execute. If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="ff91f-110">Pour les actions de règle qui s'exécutent par défaut sur le client (comme afficher une alerte de nouveau message électronique), la condition **OnLocalMachine** sera automatiquement activée, et la propriété [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) est définie à **true** pour un objet [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) côté client uniquement.</span><span class="sxs-lookup"><span data-stu-id="ff91f-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="ff91f-111">Pour les actions de règle qui s'exécutent généralement sur le serveur, définissez la propriété **Enabled** de l'objet **RuleAction** côté client uniquement pour activer la condition **OnLocalMachine**.</span><span class="sxs-lookup"><span data-stu-id="ff91f-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="ff91f-112">Cela forcera l'exécution de la règle localement sur le client.</span><span class="sxs-lookup"><span data-stu-id="ff91f-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="ff91f-113">Si la condition **OnLocalMachine** pour une règle est activée, la condition [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) est également activée lorsque la même règle est examinée par une autre machine.</span><span class="sxs-lookup"><span data-stu-id="ff91f-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="ff91f-114">Une condition de règle du type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) signale que la règle est exécutable uniquement sur un ordinateur spécifique autre que l'ordinateur actuel, et n'est pas activable ou désactivable par programmation.</span><span class="sxs-lookup"><span data-stu-id="ff91f-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="ff91f-115">Par exemple, si une règle est créée sur l'ordinateur actuel et que la condition de règle **OnLocalMachine** est activée, la règle est exécutable uniquement sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff91f-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="ff91f-116">Si la même règle est exécutée sur un autre ordinateur, la règle indique que la condition de règle **OnOtherMachine** est activée.</span><span class="sxs-lookup"><span data-stu-id="ff91f-116">If the same rule is executed on another computer, the rule will show that the **OnOtherMachine** rule condition is enabled.</span></span>

<span data-ttu-id="ff91f-117">Dans l’exemple de code suivant, DemoOnMachineOnly crée une règle et active la condition [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) et l’action [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) en définissant les propriétés **Enabled** sur **true**.</span><span class="sxs-lookup"><span data-stu-id="ff91f-117">In the following code example, DemoOnMachineOnly creates a rule and enables the [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) condition and [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) action by setting the **Enabled** properties to **true**.</span></span> <span data-ttu-id="ff91f-118">La condition **OnLocalMachine** est activée, forçant une règle côté serveur à s’exécuter localement, et les règles sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="ff91f-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="ff91f-119">Par défaut, une action **Forward** et une condition **OnlyToMe** fonctionneront sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ff91f-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="ff91f-120">Une fois la condition **OnLocalMachine** activée, les règles fonctionnent comme des règles côté client.</span><span class="sxs-lookup"><span data-stu-id="ff91f-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="ff91f-121">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ff91f-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ff91f-122">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="ff91f-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ff91f-123">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="ff91f-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a><span data-ttu-id="ff91f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff91f-124">See also</span></span>

- [<span data-ttu-id="ff91f-125">Règles</span><span class="sxs-lookup"><span data-stu-id="ff91f-125">Rules</span></span>](rules.md)

