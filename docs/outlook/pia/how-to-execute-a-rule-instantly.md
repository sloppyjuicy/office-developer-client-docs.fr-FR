---
title: Exécuter une règle instantanément
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6bb6ac5422b9785660cb3ec0020c01244002c6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708647"
---
# <a name="execute-a-rule-instantly"></a><span data-ttu-id="d2e0f-102">Exécuter une règle instantanément</span><span class="sxs-lookup"><span data-stu-id="d2e0f-102">Execute a rule instantly</span></span>

<span data-ttu-id="d2e0f-103">Cet exemple montre comment exécuter instantanément une règle à l’aide de la méthode [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) de l’objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d2e0f-103">This example shows how to execute a rule instantly by using the [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) method of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="d2e0f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2e0f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d2e0f-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d2e0f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d2e0f-p101">Vous pouvez déclencher l'exécution immédiate d'une règle en appelant la méthode **Execute** sur l'objet **Rule**. Les paramètres de la méthode **Execute** sont facultatifs ; s'ils ne sont pas spécifiés, la règle sera appliquée à tous les messages de la Boîte de réception mais pas à ses sous-dossiers, et des valeurs par défaut seront utilisées pour les paramètres. Le tableau suivant répertorie les valeurs par défaut pour les paramètres facultatifs de la méthode **Execute**.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-p101">You can cause a rule to execute immediately by calling the **Execute** method on the **Rule** object. The parameters to the **Execute** method are optional; if they are not specified, the rule will be applied to all messages in the Inbox but not to the subfolders of the Inbox, and default values for the parameters will be used. The following table lists the default values for the optional parameters of the **Execute** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2e0f-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d2e0f-109">Parameter</span></span></p></th>
<th><p><span data-ttu-id="d2e0f-110">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d2e0f-110">Default value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2e0f-111">ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d2e0f-111">ShowProgress</span></span></p></td>
<td><p><span data-ttu-id="d2e0f-112">False</span><span class="sxs-lookup"><span data-stu-id="d2e0f-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e0f-113">Dossier</span><span class="sxs-lookup"><span data-stu-id="d2e0f-113">Folder</span></span></p></td>
<td><p><span data-ttu-id="d2e0f-114">Boîte de réception</span><span class="sxs-lookup"><span data-stu-id="d2e0f-114">Inbox</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e0f-115">IncludeSubfolders</span><span class="sxs-lookup"><span data-stu-id="d2e0f-115">IncludeSubfolders</span></span></p></td>
<td><p><span data-ttu-id="d2e0f-116">False</span><span class="sxs-lookup"><span data-stu-id="d2e0f-116">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e0f-117">RuleExecuteOption</span><span class="sxs-lookup"><span data-stu-id="d2e0f-117">RuleExecuteOption</span></span></p></td>
<td><p><span data-ttu-id="d2e0f-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span><span class="sxs-lookup"><span data-stu-id="d2e0f-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d2e0f-119">Vous pouvez annuler l’exécution d’une règle à l’aide de l’Assistant Règles et alertes.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-119">You can cancel a rule execution by using the Rules and Alerts Wizard.</span></span> <span data-ttu-id="d2e0f-120">Vous pouvez aussi annuler l’exécution d’une règle en définissant le paramètre *ShowProgress* sur **true**, puis en annulant la boîte de dialogue de progression.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-120">You can also cancel a rule execution by setting the *ShowProgress* parameter to **true** and then canceling the progress dialog box.</span></span> <span data-ttu-id="d2e0f-121">Une fois que vous avez annulé la boîte de dialogue de progression, **Execute** renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-121">Once you cancel the progress dialog box, **Execute** will return an error.</span></span>

<span data-ttu-id="d2e0f-122">Dans l’exemple de code suivant, ExecuteManagerRule obtient la règle qui a été créée dans la procédure CreateManagerRule de la rubrique [Créer une règle pour classer les éléments de courrier provenant d’un responsable et les marquer pour suivi](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="d2e0f-122">In the following code example, ExecuteManagerRule gets the rule that was created in the procedure CreateManagerRule from the topic [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span> <span data-ttu-id="d2e0f-123">ExecuteManagerRule vérifie ensuite si la règle n’est pas une référence NULL.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-123">ExecuteManagerRule then checks whether the rule is not a null reference.</span></span> <span data-ttu-id="d2e0f-124">Si ce n’est pas le cas, ExecuteManagerRule appelle la méthode **Execute** sur la règle avec les paramètres par défaut, exécutant immédiatement la règle.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-124">If the rule is not a null reference, ExecuteManagerRule calls the **Execute** method on the rule with default parameters, instantly executing the rule.</span></span>

> [!NOTE]
> <span data-ttu-id="d2e0f-p104">Pour appliquer une règle une fois, indépendamment du fait que la propriété [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) retourne **true**, utilisez la méthode **Rule.Execute**. Pour appliquer la règle pour la session actuelle et au-delà de cette session, utilisez à la fois la propriété **Rule.Enabled** et la méthode [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) .</span><span class="sxs-lookup"><span data-stu-id="d2e0f-p104">To apply a rule once, regardless of whether the [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) property returns **true**, use the **Rule.Execute** method. To apply the rule for the current session and beyond the current session, use both the **Rule.Enabled** property and the [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) method.</span></span>

<span data-ttu-id="d2e0f-127">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d2e0f-128">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d2e0f-129">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="d2e0f-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="d2e0f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2e0f-130">See also</span></span>

- [<span data-ttu-id="d2e0f-131">Règles</span><span class="sxs-lookup"><span data-stu-id="d2e0f-131">Rules</span></span>](rules.md)

