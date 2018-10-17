---
title: Création d’un élément de tâche
TOCTitle: Create a task item
ms:assetid: d458dd31-2771-4a3c-a713-13c7e4e02a74
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184644(v=office.15)
ms:contentKeyID: 55119894
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 467d715e0fca1adfd835b11c36889dff3dbf145d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406805"
---
# <a name="create-a-task-item"></a><span data-ttu-id="b24a8-102">Création d’un élément de tâche</span><span class="sxs-lookup"><span data-stu-id="b24a8-102">Create a task item</span></span>

<span data-ttu-id="b24a8-103">Cet exemple montre comment créer un élément de tâche à l’aide de la méthode [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b24a8-103">This example shows how to create a task item by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="b24a8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b24a8-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b24a8-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b24a8-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="b24a8-106">Dans l’exemple de code suivant, CreateToDoItemExample crée un élément de tâche en appelant la méthode **MarkAsTask** sur l’élément, puis en enregistrant l’élément.</span><span class="sxs-lookup"><span data-stu-id="b24a8-106">In the following code example, CreateToDoItemExample creates a to-do item by calling the **MarkAsTask** method on the item and then saving the item.</span></span> <span data-ttu-id="b24a8-107">L’exemple permet de marquer l’élément pour le suivre le lendemain et définit un rappel pour demain, 10h</span><span class="sxs-lookup"><span data-stu-id="b24a8-107">The example marks the item for follow-up tomorrow and sets a reminder for tomorrow at 10:00 A.M.</span></span> <span data-ttu-id="b24a8-108">à l’aide des propriétés [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) et [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b24a8-108">by using the [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) and [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)) properties.</span></span> <span data-ttu-id="b24a8-109">L’exemple utilise ensuite la méthode [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) pour enregistrer l’élément.</span><span class="sxs-lookup"><span data-stu-id="b24a8-109">The example then uses the [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) method to save the item.</span></span>

<span data-ttu-id="b24a8-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b24a8-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="b24a8-111">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="b24a8-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="b24a8-112">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="b24a8-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateToDoItemExample()
{
    // Date operations
    DateTime today = DateTime.Parse("10:00 AM");
    TimeSpan duration = TimeSpan.FromDays(1);
    DateTime tomorrow = today.Add(duration);
    Outlook.MailItem mail = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Find(
        "[MessageClass]='IPM.Note'") as Outlook.MailItem;
    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkTomorrow);
    mail.TaskStartDate = today;
    mail.ReminderSet = true;
    mail.ReminderTime = tomorrow;
    mail.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="b24a8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b24a8-113">See also</span></span>

- [<span data-ttu-id="b24a8-114">Tâches</span><span class="sxs-lookup"><span data-stu-id="b24a8-114">Tasks</span></span>](tasks.md)

