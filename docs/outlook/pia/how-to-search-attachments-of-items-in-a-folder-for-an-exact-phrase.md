---
title: Recherche d’une expression exacte dans les pièces jointes des éléments d’un dossier
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609825(v=office.15)
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 915ddd65e8227f6cc720c4494ed1767deed121b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406154"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="a3de8-102">Recherche d’une expression exacte dans les pièces jointes des éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="a3de8-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="a3de8-103">Cet exemple recherche la chaîne de recherche exacte « office » dans les pièces jointes aux éléments figurant dans la Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="a3de8-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="a3de8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3de8-104">Example</span></span>

<span data-ttu-id="a3de8-105">Cet exemple de code utilise une syntaxe DASL (DAV Searching and Locating) pour spécifier une requête.</span><span class="sxs-lookup"><span data-stu-id="a3de8-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="a3de8-106">Pour construire le filtre, l’exemple de code vérifie d’abord si la recherche instantanée est activée dans la banque par défaut pour déterminer s’il faut utiliser le mot clé **ci\_phrasematch** pour trouver une correspondance exacte avec « office » dans toutes les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="a3de8-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the ci_phrasematch keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="a3de8-107">L’exemple applique ensuite le filtre à la méthode [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) sur la Boîte de réception et obtient les résultats dans un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a3de8-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="a3de8-108">L’exemple de code affiche ensuite l’objet de chaque élément renvoyé dans l’objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="a3de8-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="a3de8-109">L’exemple de code spécifie la propriété **Attachments** d’un élément à l’aide d’une représentation d’espace de noms, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span><span class="sxs-lookup"><span data-stu-id="a3de8-109">The code sample specifies the **Attachments** property of an item using the namespace representation,  https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="a3de8-110">La syntaxe à employer pour utiliser le mot clé **ci\_phrasematch** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="a3de8-110">The syntax for using the ci_phrasematch keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="a3de8-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a3de8-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="a3de8-112">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="a3de8-112">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="a3de8-113">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="a3de8-113">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```


```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a3de8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3de8-114">See also</span></span>

- [<span data-ttu-id="a3de8-115">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="a3de8-115">Search and Filter</span></span>](search-and-filter.md)

