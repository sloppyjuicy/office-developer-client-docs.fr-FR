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
# <a name="get-and-enumerate-selected-conversations"></a><span data-ttu-id="333b3-102">Obtention et énumération des conversations sélectionnées</span><span class="sxs-lookup"><span data-stu-id="333b3-102">Get and enumerate selected conversations</span></span>

<span data-ttu-id="333b3-103">Cet exemple obtient et énumère les conversations sélectionnées à l’aide de la méthode [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="333b3-103">This example obtains and enumerates selected conversations by using the [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="333b3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="333b3-104">Example</span></span>

<span data-ttu-id="333b3-p101">Microsoft Outlook peut être défini de manière à afficher les éléments de la Boîte de réception par conversation. Si un utilisateur effectue une sélection dans la Boîte de réception, vous pouvez obtenir cette sélection par programme, y compris les en-têtes et les éléments de conversation. L'exemple de code de cette rubrique montre comment obtenir une sélection dans la Boîte de réception et comment énumérer les éléments de courrier dans chaque conversation de la sélection.</span><span class="sxs-lookup"><span data-stu-id="333b3-p101">Microsoft Outlook can be set to display items in the Inbox by conversation. If a user makes a selection in the Inbox, you can obtain the selection programmatically, including conversation headers and conversation items. The code example in this topic shows how to obtain a selection in the Inbox and enumerate the mail items in each conversation in the selection.</span></span>

<span data-ttu-id="333b3-108">L’exemple contient une méthode, DemoConversationHeadersFromSelection.</span><span class="sxs-lookup"><span data-stu-id="333b3-108">The example contains one method, DemoConversationHeadersFromSelection.</span></span> <span data-ttu-id="333b3-109">La méthode définit l’affichage actuel sur la boîte de réception, puis vérifie si l’affichage actuel est un affichage tableau qui indique des conversations triées par date.</span><span class="sxs-lookup"><span data-stu-id="333b3-109">The method sets the current view to the Inbox, and then checks whether the current view is a table view that displays conversations sorted by date.</span></span> <span data-ttu-id="333b3-110">Pour obtenir une sélection, y compris les objets [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) sélectionnés, DemoConversationHeadersFromSelection utilise la méthode **GetSelection** de l’objet [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)), en spécifiant la constante [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) comme un argument.</span><span class="sxs-lookup"><span data-stu-id="333b3-110">To obtain a selection, including any selected [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) objects, DemoConversationHeadersFromSelection uses the **GetSelection** method of the [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object, specifying the [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) constant as an argument.</span></span> <span data-ttu-id="333b3-111">Si les en-têtes de conversation sont sélectionnés, DemoConversationHeadersFromSelection utilise l’objet [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) pour énumérer les éléments dans chaque conversation sélectionnée, puis affiche l’objet de ces éléments de conversation qui sont des objets [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="333b3-111">If conversation headers are selected, DemoConversationHeadersFromSelection uses the [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) object to enumerate items in each selected conversation, and then displays the subject of those conversation items that are [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects.</span></span>

<span data-ttu-id="333b3-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="333b3-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="333b3-113">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="333b3-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="333b3-114">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="333b3-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="333b3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="333b3-115">See also</span></span>

- [<span data-ttu-id="333b3-116">Conversations</span><span class="sxs-lookup"><span data-stu-id="333b3-116">Conversations</span></span>](conversations.md)

