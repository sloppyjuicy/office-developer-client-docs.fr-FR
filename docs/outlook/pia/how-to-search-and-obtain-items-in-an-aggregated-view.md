---
title: Recherche et obtention des éléments dans une vue agrégée
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 653d9fd0fe244f67298dfa86355fb14f52fcc436
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560472"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a>Recherche et obtention des éléments dans une vue agrégée

Cet exemple montre comment rechercher des éléments dans plusieurs dossiers et banques d’informations et renvoyer ces éléments dans une vue Table agrégée.

## <a name="example"></a>Exemple

La méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) de l'objet [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) peut retourner, dans une vue agrégée, un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) qui contient des éléments d'un ou plusieurs dossiers dans la même banque ou couvrant plusieurs banques. Ceci est particulièrement utile lorsque vous souhaitez accéder à des éléments retournés par une recherche (par exemple une recherche sur tous les éléments de messagerie contenus dans une banque). Cette rubrique illustre comment utiliser la **Recherche instantanée** pour rechercher parmi les éléments reçus ceux envoyés par le Responsable de l'utilisateur actif et marqués comme importants, puis afficher l'objet de chaque résultat de recherche.

Dans l’exemple de code suivant, la méthode **GetItemsInView** vérifie si le compte de la banque de remise principale de l’utilisateur actuel est un compte Exchange, si l’utilisateur actuel a un manager, et si la **recherche instantanée** est opérationnelle dans la banque par défaut de la session. Étant donné que la recherche repose sur la méthode [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) de l’objet [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) et que le résultat de la recherche est obtenu au moyen de la méthode **GetTable**, **GetItemsInView** crée un objet **Explorer**, affiche la Boîte de réception dans cet objet et l’utilise pour configurer la recherche. 

**GetItemsInView** recherche dans tous les dossiers du type [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) les éléments envoyés par le manager de l’utilisateur actuel et marqués comme importants. Une fois que **GetItemsInView** a appelé la méthode [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), les résultats de recherche sont affichés dans l’Explorateur, y compris les éléments d’autres dossiers et banques qui répondent aux critères de recherche. **GetItemsInView** obtient un objet **TableView** qui contient le mode Explorateur des résultats de recherche. En faisant appel à la méthode **GetTable** de l’objet **TableView**, **GetItemsInView** obtient ensuite un objet **Table** qui contient les éléments agrégés renvoyés par la recherche. Pour finir, **GetItemsInView** affiche la colonne d’objet de chaque ligne de l’objet **Table** qui représente un élément dans les résultats de recherche.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetItemsInView()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;

    // Check whether the current user uses the Exchange Server.
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();

        // Check whether the current user has a manager.
        if (manager != null)
        {
            string managerName = manager.Name;

            // Check whether Instant Search is enabled and 
            // operational in the default store.
            if (Application.Session.DefaultStore.IsInstantSearchEnabled)
            {
                Outlook.Folder inbox =
                    Application.Session.GetDefaultFolder(
                    Outlook.OlDefaultFolders.olFolderInbox);

                // Create a new explorer to display the Inbox as
                // the current folder.
                Outlook.Explorer explorer =
                    Application.Explorers.Add(inbox,
                    Outlook.OlFolderDisplayMode.olFolderDisplayNormal);

                // Make the new explorer visible.
                explorer.Display;

                // Search for items from the manager marked important, 
                // from all folders of the same item type as the current folder, 
                // which is the MailItem item type.
                string searchFor =
                    "from:" + "\"" + managerName 
                    + "\"" + " importance:high";
                explorer.Search(searchFor,
                    Outlook.OlSearchScope.olSearchScopeAllFolders);

                // Any search results are displayed in that new explorer
                // in an aggregated table view.
                Outlook.TableView tableView = 
                    explorer.CurrentView as Outlook.TableView;

                // Use GetTable of that table view to obtain items in that
                // aggregated view in a Table object.
                Outlook.Table table = tableView.GetTable();
                while (!table.EndOfTable)
                {
                    // Then display each row in the Table object
                    // that represents an item in the search results.
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

