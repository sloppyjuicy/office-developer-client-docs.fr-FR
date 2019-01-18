---
title: Afficher les éléments de demande de tâche envoyés à un destinataire
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9ab5e830003fbfb64b44fc9e0d813c7a7c5163bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726049"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>Afficher les éléments de demande de tâche envoyés à un destinataire

Cet exemple montre comment afficher tous les éléments de demande de tâche qui se trouvent dans la boîte de réception d’un destinataire.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Un objet [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) représente une demande d’affectation d’une tâche à un autre utilisateur. L’objet **TaskRequestItem** est créé lorsque l’élément est reçu dans la boîte de réception du destinataire. Dans l’exemple de code suivant, ShowTaskRequests filtre la boîte de réception d’un destinataire, crée un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), puis insère une ligne pour chaque élément dont la propriété [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) a la valeur **IPM.TaskRequest**. L’objet de chaque tâche dans le dossier Boîte de réception du destinataire est ensuite inscrit dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowTaskRequests()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).GetTable
        (filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Tâches](tasks.md)

