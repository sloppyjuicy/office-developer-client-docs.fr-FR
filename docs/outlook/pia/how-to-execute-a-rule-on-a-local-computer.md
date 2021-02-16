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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320348"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="1d95c-102">Exécuter une règle sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="1d95c-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="1d95c-103">Cet exemple montre comment exécuter une règle sur un ordinateur local à l’aide de la propriété [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) de l’objet [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1d95c-103">This example shows how to execute a rule on a local computer by using the [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="1d95c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1d95c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1d95c-105">L’exemple de code suivant est extrait du livre[programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (non traduit)..</span><span class="sxs-lookup"><span data-stu-id="1d95c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="1d95c-p101">Si votre boîte aux lettres est hébergée sur un serveur Exchange, vous pouvez exécuter une règle sur le serveur Exchange ou sur le client Outlook. Si vous exécutez la règle sur le serveur, vous n’avez pas besoin d’exécuter Outlook pour évaluer les conditions de la règle et exécuter ses actions. Si vous exécutez la règle sur le client, vous devez exécuter Outlook. Si la propriété [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) de l’objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) retourne **true**, la règle doit être exécutée sur le client.</span><span class="sxs-lookup"><span data-stu-id="1d95c-p101">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client. If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed. If the rule is executed on the client, Outlook must be running for the rule to execute. If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="1d95c-110">En cas d’exécution d’actions de règle par défaut sur le client (comme l’affichage d’une alerte de nouveau message électronique), la condition **OnLocalMachine** s’active automatiquement, tandis que le système définit la propriété [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) sur **true** pour un objet [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) côté client.</span><span class="sxs-lookup"><span data-stu-id="1d95c-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="1d95c-111">Si des actions de règle s’exécutent globalement sur le serveur, veuillez définir la propriété **Enabled** de l’objet **RuleAction** côté client pour activer la condition **OnLocalMachine**.</span><span class="sxs-lookup"><span data-stu-id="1d95c-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="1d95c-112">Vous forcez ainsi l’exécution de la règle sur le client en local.</span><span class="sxs-lookup"><span data-stu-id="1d95c-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="1d95c-113">Si la condition **OnLocalMachine** d’une règle s’active, la condition [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) s’active aussi, lorsqu’une autre machine examine la même règle.</span><span class="sxs-lookup"><span data-stu-id="1d95c-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="1d95c-114">Une condition de règle du type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indique que vous pouvez uniquement exécuter la règle sur un ordinateur distinct de l’ordinateur actuel, et que vous ne pouvez pas l’activer ou la désactiver par programmation.</span><span class="sxs-lookup"><span data-stu-id="1d95c-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="1d95c-115">Par exemple, si vous créez une règle sur l’ordinateur actuel tout en ayant activé la condition de règle **OnLocalMachine**, vous devez exécuter cette règle sur cet ordinateur, et seulement lui.</span><span class="sxs-lookup"><span data-stu-id="1d95c-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="1d95c-116">Si vous exécutez cette règle sur un autre ordinateur, la règle indique que la condition de règle **OnOtherMachine** est active.</span><span class="sxs-lookup"><span data-stu-id="1d95c-116">If the same rule is executed on another computer, the rule will show that the **OnOtherMachine** rule condition is enabled.</span></span>

<span data-ttu-id="1d95c-117">Dans l’exemple de code suivant, DemoOnMachineOnly crée une règle et active la condition [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) et l’action [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) en définissant les propriétés **Enabled** sur **true**.</span><span class="sxs-lookup"><span data-stu-id="1d95c-117">In the following code example, DemoOnMachineOnly creates a rule and enables the [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) condition and [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) action by setting the **Enabled** properties to **true**.</span></span> <span data-ttu-id="1d95c-118">La condition **OnLocalMachine** s’active, forçant l’exécution en local d’une règle côté serveur. Puis le système enregistre les règles.</span><span class="sxs-lookup"><span data-stu-id="1d95c-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="1d95c-119">Par défaut, une action **Forward** et une condition **OnlyToMe** fonctionneront sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1d95c-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="1d95c-120">Une fois la condition **OnLocalMachine** activée, les règles fonctionnent comme des règles côté client.</span><span class="sxs-lookup"><span data-stu-id="1d95c-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="1d95c-121">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1d95c-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1d95c-122">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="1d95c-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1d95c-123">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="1d95c-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1d95c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d95c-124">See also</span></span>

- [<span data-ttu-id="1d95c-125">Règles</span><span class="sxs-lookup"><span data-stu-id="1d95c-125">Rules</span></span>](rules.md)

