---
title: Recherche dans un dossier d’une expression employée dans le corps des éléments
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc8e0fb2b82ae9660e292a6ec1dea70e82fe36ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316029"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a><span data-ttu-id="3a19d-102">Recherche dans un dossier d’une expression employée dans le corps des éléments</span><span class="sxs-lookup"><span data-stu-id="3a19d-102">Search for a phrase in the body of items in a folder</span></span>

<span data-ttu-id="3a19d-103">Cet exemple recherche la chaîne « office » dans le corps des éléments de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="3a19d-103">This example searches for the string "office" in the Body of items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="3a19d-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a19d-104">Example</span></span>

<span data-ttu-id="3a19d-105">Cet exemple de code utilise une syntaxe DASL (DAV Searching and Locating) pour spécifier une requête.</span><span class="sxs-lookup"><span data-stu-id="3a19d-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="3a19d-106">Pour construire le filtre, l’exemple de code vérifie d’abord si la recherche instantanée est activée dans la banque par défaut afin de déterminer s’il faut utiliser le mot clé **ci\_phrasematch** pour une correspondance de phrase exacte de « office » dans le corps de l’élément, ou le mot clé **like** pour trouver toute occurrence de « office » comme chaîne ou sous-chaîne exacte dans le corps de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3a19d-106">To construct the filter, the code sample first checks if Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match of "office" in the item body, or the **like** keyword to match any occurrence of "office" as an exact string or a substring in the item body.</span></span> <span data-ttu-id="3a19d-107">L’exemple applique ensuite le filtre à la méthode [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) sur la Boîte de réception et obtient les résultats dans un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3a19d-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="3a19d-108">L’exemple de code affiche ensuite l’objet de chaque élément renvoyé dans l’objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="3a19d-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="3a19d-109">L’exemple de code spécifie la propriété **Body** en utilisant la représentation d’espace de noms urn:schemas:httpmail:textdescription.</span><span class="sxs-lookup"><span data-stu-id="3a19d-109">The code sample specifies the **Body** property by using the namespace representation urn:schemas:httpmail:textdescription.</span></span>

<span data-ttu-id="3a19d-110">La syntaxe à employer pour utiliser le mot clé **ci\_phrasematch** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3a19d-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="3a19d-111">La syntaxe à employer pour utiliser le mot clé **like** pour la correspondance de préfixes est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3a19d-111">The syntax for using the **like** keyword for prefix matching is:</span></span>

`<PropertySchemaName> like <Token>%`

<span data-ttu-id="3a19d-112">La syntaxe à employer pour utiliser le mot clé **like** pour la correspondance de sous-chaînes est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3a19d-112">The syntax for using the **like** keyword for any substring matching is:</span></span>

`<PropertySchemaName> like %<Token>%`

<span data-ttu-id="3a19d-113">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3a19d-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3a19d-114">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="3a19d-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3a19d-115">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="3a19d-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3a19d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a19d-116">See also</span></span>

- [<span data-ttu-id="3a19d-117">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="3a19d-117">Search and filter</span></span>](search-and-filter.md)

