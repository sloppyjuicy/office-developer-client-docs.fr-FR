---
title: Recherche d’une expression exacte dans les pièces jointes des éléments d’un dossier
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3d14da44731810308d57ba0e70f9651f3105aad0
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773714"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="6d0bc-102">Recherche d’une expression exacte dans les pièces jointes des éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="6d0bc-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="6d0bc-103">Cet exemple recherche la chaîne de recherche exacte « office » dans les pièces jointes aux éléments figurant dans la Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="6d0bc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6d0bc-104">Example</span></span>

<span data-ttu-id="6d0bc-105">Cet exemple de code utilise une syntaxe DASL (DAV Searching and Locating) pour spécifier une requête.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="6d0bc-106">Pour construire le filtre, l’exemple de code vérifie d’abord si la recherche instantanée est activée dans la banque par défaut pour déterminer s’il faut utiliser le mot clé **ci\_phrasematch** pour trouver une correspondance exacte avec « office » dans toutes les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="6d0bc-107">L’exemple applique ensuite le filtre à la méthode [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) sur la Boîte de réception et obtient les résultats dans un objet [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="6d0bc-107">The sample then applies the filter to the [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) method on the Inbox and obtains the results in a [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia) object.</span></span> <span data-ttu-id="6d0bc-108">L’exemple de code affiche ensuite l’objet de chaque élément renvoyé dans l’objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="6d0bc-109">L’exemple de code spécifie la propriété **Attachments** d’un élément à l’aide d’une représentation d’espace de noms, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-109">The code sample specifies the **Attachments** property of an item using the namespace representation, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="6d0bc-110">La syntaxe à employer pour utiliser le mot clé **ci\_phrasematch** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6d0bc-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="6d0bc-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6d0bc-112">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6d0bc-113">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
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
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
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

## <a name="see-also"></a><span data-ttu-id="6d0bc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d0bc-114">See also</span></span>

- [<span data-ttu-id="6d0bc-115">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="6d0bc-115">Search and filter</span></span>](search-and-filter.md)

