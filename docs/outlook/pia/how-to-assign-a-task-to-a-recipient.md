---
title: Affectation d’une tâche à un destinataire
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 55063cfd6c448fe32a9d4348069266b9e4a8b566
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406329"
---
# <a name="assign-a-task-to-a-recipient"></a>Affectation d’une tâche à un destinataire

Cet exemple montre comment créer une tâche et l’affecter à un destinataire.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Dans l’exemple de code suivant, AssignTaskExample crée un objet [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) et spécifie les valeurs pour les propriétés [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)) et [DueDate ](https://msdn.microsoft.com/library/bb612307\(v=office.15\)). La méthode [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) indique que la tâche est affectée. Une fois qu’un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) est ajouté à l’objet **TaskItem** à l’aide de la méthode [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)), la méthode [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) envoie la tâche au destinataire.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AssignTaskExample()
{
    Outlook.TaskItem task = Application.CreateItem(
        Outlook.OlItemType.olTaskItem) as Outlook.TaskItem;
    task.Subject = "Tax Preparation";
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM");
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM");
    Outlook.RecurrencePattern pattern =
        task.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly;
    pattern.PatternStartDate = DateTime.Parse("4/1/2007");
    pattern.NoEndDate = true;
    task.ReminderSet = true;
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM");
    task.Assign();
    task.Recipients.Add("accountant@example.com");
    task.Recipients.ResolveAll();
    task.Send();
}
```

## <a name="see-also"></a>Voir aussi

- [Tâches](tasks.md)

