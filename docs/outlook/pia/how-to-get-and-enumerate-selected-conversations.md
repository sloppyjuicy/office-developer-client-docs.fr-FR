---
title: Obtention et énumération des conversations sélectionnées
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d71fc1d582abebc8cb00f4885ec5b5ba348228c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320313"
---
# <a name="get-and-enumerate-selected-conversations"></a>Obtention et énumération des conversations sélectionnées

Cet exemple obtient et énumère les conversations sélectionnées à l’aide de la méthode [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).

## <a name="example"></a>Exemple

Microsoft Outlook peut être défini de manière à afficher les éléments de la Boîte de réception par conversation. Si un utilisateur effectue une sélection dans la Boîte de réception, vous pouvez obtenir cette sélection par programme, y compris les en-têtes et les éléments de conversation. L'exemple de code de cette rubrique montre comment obtenir une sélection dans la Boîte de réception et comment énumérer les éléments de courrier dans chaque conversation de la sélection.

L’exemple contient une méthode, DemoConversationHeadersFromSelection. La méthode définit l’affichage actuel sur la boîte de réception, puis vérifie si l’affichage actuel est un affichage tableau qui indique des conversations triées par date. Pour obtenir une sélection, y compris les objets [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) sélectionnés, DemoConversationHeadersFromSelection utilise la méthode **GetSelection** de l’objet [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)), en spécifiant la constante [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) comme un argument. Si les en-têtes de conversation sont sélectionnés, DemoConversationHeadersFromSelection utilise l’objet [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) pour énumérer les éléments dans chaque conversation sélectionnée, puis affiche l’objet de ces éléments de conversation qui sont des objets [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoConversationHeadersFromSelection()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType ==
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view =
            inbox.CurrentView as Outlook.TableView;
        if (view.ShowConversationByDate == true)
        {
            Outlook.Selection selection =
                Application.ActiveExplorer().Selection;
            Debug.WriteLine("Selection.Count = " + selection.Count);
            // Call GetSelection to create a Selection object
            // that contains ConversationHeader objects.
            Outlook.Selection convHeaders =
                selection.GetSelection(
                Outlook.OlSelectionContents.olConversationHeaders)
                as Outlook.Selection;
            Debug.WriteLine("Selection.Count (ConversationHeaders) = " 
                + convHeaders.Count);
            if (convHeaders.Count >= 1)
            {
                foreach (Outlook.ConversationHeader convHeader in convHeaders)
                {
                    // Enumerate the items in the ConversationHeader.
                    Outlook.SimpleItems items = convHeader.GetItems();
                    for (int i = 1; i <= items.Count; i++)
                    {
                        // Enumerate only MailItems in this example.
                        if (items[i] is Outlook.MailItem)
                        {
                            Outlook.MailItem mail = 
                                items[i] as Outlook.MailItem;
                            Debug.WriteLine(mail.Subject 
                                + " Received:" + mail.ReceivedTime);
                        }
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Conversations](conversations.md)

