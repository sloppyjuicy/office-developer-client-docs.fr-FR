---
title: Obtention et affichage des éléments d’une conversation
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5f130edfbfb742f727e9b74779736b380547ff02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623683"
---
# <a name="get-and-display-items-in-a-conversation"></a>Obtention et affichage des éléments d’une conversation

Cet exemple montre comment obtenir et afficher les éléments de courrier dans une conversation.

## <a name="example"></a>Exemple

Dans l’exemple de code suivant, DemoConversation obtient un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), puis détermine la banque de l’objet **MailItem** à l’aide de la propriété [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) de l’objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)). DemoConversation vérifie ensuite si la propriété [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) a la valeur **true** ; si elle a cette valeur **true**, l’exemple de code obtient l’objet [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) à l’aide de la méthode [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)). Si l'objet **Conversation** n'est pas une référence null, l'exemple obtient l'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) associé qui contient chaque élément de la conversation à l'aide de la méthode [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)) . 

L’exemple énumère ensuite chaque élément contenu dans **Table** puis appelle EnumerateConversation sur chaque élément pour accéder aux nœuds enfants de chaque élément. EnumerateConversation prend un objet **Conversation** et obtient les nœuds enfants à l’aide de la méthode [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)). EnumerateConversation est appelée de façon récursive jusqu’à ce qu’il n’y ait plus de nœuds enfants. Chaque élément de conversation est ensuite présenté à l’utilisateur.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
void DemoConversation()
{
    object selectedItem = 
        Application.ActiveExplorer().Selection[1];
    // For this example, you will work only with 
    //MailItem. Other item types such as
    //MeetingItem and PostItem can participate 
    //in Conversation.
    if (selectedItem is Outlook.MailItem)
    {
        // Cast selectedItem to MailItem.
        Outlook.MailItem mailItem =
            selectedItem as Outlook.MailItem; ;
        // Determine store of mailItem.
        Outlook.Folder folder = mailItem.Parent
            as Outlook.Folder;
        Outlook.Store store = folder.Store;
        if (store.IsConversationEnabled == true)
        {
            // Obtain a Conversation object.
            Outlook.Conversation conv =
                mailItem.GetConversation();
            // Check for null Conversation.
            if (conv != null)
            {
                // Obtain Table that contains rows 
                // for each item in Conversation.
                Outlook.Table table = conv.GetTable();
                Debug.WriteLine("Conversation Items Count: " +
                    table.GetRowCount().ToString());
                Debug.WriteLine("Conversation Items from Table:");
                while (!table.EndOfTable)
                {
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]
                        + " Modified: "
                        + nextRow["LastModificationTime"]);
                }
                Debug.WriteLine("Conversation Items from Root:");
                // Obtain root items and enumerate Conversation.
                Outlook.SimpleItems simpleItems 
                    = conv.GetRootItems();
                foreach (object item in simpleItems)
                {
                    // In this example, enumerate only MailItem type.
                    // Other types such as PostItem or MeetingItem
                    // can appear in Conversation.
                    if (item is Outlook.MailItem)
                    {
                        Outlook.MailItem mail = item
                            as Outlook.MailItem;
                        Outlook.Folder inFolder =
                            mail.Parent as Outlook.Folder;
                        string msg = mail.Subject
                            + " in folder " + inFolder.Name;
                        Debug.WriteLine(msg);
                    }
                    // Call EnumerateConversation 
                    // to access child nodes of root items.
                    EnumerateConversation(item, conv);
                }
            }
        }
    }
}

void EnumerateConversation(object item,
    Outlook.Conversation conversation)
{
    Outlook.SimpleItems items =
        conversation.GetChildren(item);
    if (items.Count > 0)
    {
        foreach (object myItem in items)
        {
            // In this example, enumerate only MailItem type.
            // Other types such as PostItem or MeetingItem
            // can appear in Conversation.
            if (myItem is Outlook.MailItem)
            {
                Outlook.MailItem mailItem =
                    myItem as Outlook.MailItem;
                Outlook.Folder inFolder =
                    mailItem.Parent as Outlook.Folder;
                string msg = mailItem.Subject
                    + " in folder " + inFolder.Name;
                Debug.WriteLine(msg);
            }
            // Continue recursion.
            EnumerateConversation(myItem, conversation);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Conversations](conversations.md)

