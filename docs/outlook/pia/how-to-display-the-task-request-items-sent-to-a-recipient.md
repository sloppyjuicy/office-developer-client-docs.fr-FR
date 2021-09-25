---
title: Afficher les éléments de demande de tâche envoyés à un destinataire
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 753de29eb19ec73ebb7cf1fb8e407d02e55c1b41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616333"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>Afficher les éléments de demande de tâche envoyés à un destinataire

Cet exemple montre comment afficher tous les éléments de demande de tâche qui se trouvent dans la boîte de réception d’un destinataire.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Un objet [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) représente une demande d’affectation d’une tâche à un autre utilisateur. L’objet **TaskRequestItem** est créé lorsque l’élément est reçu dans la boîte de réception du destinataire. Dans l’exemple de code suivant, ShowTaskRequests filtre la boîte de réception d’un destinataire, crée un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), puis insère une ligne pour chaque élément dont la propriété [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) a la valeur **IPM.TaskRequest**. L’objet de chaque tâche dans le dossier Boîte de réception du destinataire est ensuite inscrit dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

