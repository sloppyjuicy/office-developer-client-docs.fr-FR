---
title: Filtrage des rendez-vous périodiques et recherche d’une chaîne dans l’objet
TOCTitle: Filter recurring appointments and search for a string in the subject
ms:assetid: 997186aa-5264-4b19-bed6-51c38831c03d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611267(v=office.15)
ms:contentKeyID: 55119891
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6bda9cc663af1d1b9167ec78da286fe1c1991d40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320264"
---
# <a name="filter-recurring-appointments-and-search-for-a-string-in-the-subject"></a><span data-ttu-id="5add7-102">Filtrage des rendez-vous périodiques et recherche d’une chaîne dans l’objet</span><span class="sxs-lookup"><span data-stu-id="5add7-102">Filter recurring appointments and search for a string in the subject</span></span>

<span data-ttu-id="5add7-103">Cet exemple filtre les rendez-vous périodiques compris dans une plage de dates dans un dossier Calendrier, puis recherche la chaîne « office » dans l’objet de ces rendez-vous de deux manières différentes.</span><span class="sxs-lookup"><span data-stu-id="5add7-103">This example filters recurring appointments that fall within a date range in a Calendar folder, and then searches in two ways for the string "office" in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="5add7-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5add7-104">Example</span></span>

<span data-ttu-id="5add7-105">Pour filtrer des rendez-vous périodiques, cet exemple de code utilise la collection [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) à la place de l’objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), car l’objet **Table** renvoie uniquement les rendez-vous principaux de la collection et n’inclut pas les éléments périodiques du dossier.</span><span class="sxs-lookup"><span data-stu-id="5add7-105">To filter recurring appointments, this code sample uses the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection instead of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, because the **Table** object returns only the master series appointments and does not include recurring items in the folder.</span></span> <span data-ttu-id="5add7-106">Pour inclure les rendez-vous périodiques pendant l’appel de la méthode [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) ou [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)), l’exemple de code définit la propriété [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) de la collection **Items**, puis trie les rendez-vous du dossier selon la date indiquée dans la propriété [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5add7-106">To include recurring appointments when calling the [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) or [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method, the code sample sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the **Items** collection, and then sorts appointments in the folder by their [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span> <span data-ttu-id="5add7-107">Il utilise ensuite une requête Jet pour indiquer les dates de début et de fin des périodicités.</span><span class="sxs-lookup"><span data-stu-id="5add7-107">It then uses a Jet query to specify start and end dates for the recurrences.</span></span>

<span data-ttu-id="5add7-108">Après avoir obtenu une collection d’éléments de rendez-vous périodiques **Items** compris dans la plage de dates spécifiée, l’exemple de code effectue deux autres recherches à l’aide des requêtes DASL (DAV Searching and Locating).</span><span class="sxs-lookup"><span data-stu-id="5add7-108">After obtaining an **Items** collection of recurring appointment items that fall within the specified range of dates, the code sample carries out two more searches using DAV Searching and Locating (DASL) queries.</span></span> <span data-ttu-id="5add7-109">La première recherche utilise les méthodes **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\))et le mot clé **like** pour rechercher tous les éléments dont la sous-chaîne « office » figure dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="5add7-109">The first search uses **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\)), and the **like** keyword to search for items that have "office" as a substring in the subject.</span></span> <span data-ttu-id="5add7-110">La deuxième recherche utilise la méthode **Items.Restrict** et le mot clé **ci\_startswith** pour rechercher tous les éléments dont l’objet commence par « office ».</span><span class="sxs-lookup"><span data-stu-id="5add7-110">The second search uses the **Items.Restrict** method and the **ci\_startswith** keyword to search for items that have subjects beginning with "office."</span></span>

<span data-ttu-id="5add7-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5add7-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5add7-112">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="5add7-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5add7-113">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="5add7-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SearchRecurringAppointments()
    Dim appt As Outlook.AppointmentItem = Nothing
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), _
        Outlook.Folder)
    ' Set start value
    Dim startTime As DateTime = New DateTime(2006, 8, 9, 0, 0, 0)
    ' Set end value
    Dim endTime As DateTime = New DateTime(2006, 12, 14, 0, 0, 0)
    ' Initial restriction is Jet query for date range
    Dim filter1 As String = "[Start] >= '" & startTime.ToString("g") _
        & "' AND [End] <= '" & endTime.ToString("g") & "'"
    Dim calendarItems As Outlook.Items = folder.Items.Restrict(filter1)
    calendarItems.IncludeRecurrences = True
    calendarItems.Sort("[Start]")
    ' Must use 'like' comparison for Find/FindNext
    Dim filter2 As String
    filter2 = "@SQL=" & _
        Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & _
        " like '%Office%'"
    ' Create DASL query for additional Restrict method
    Dim filter3 As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            ci_startswith 'Office'"
    Else
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            like '%Office%'"
    End If
    ' Use Find and FindNext methods
    appt = CType(calendarItems.Find(filter2), Outlook.AppointmentItem)
    While Not (appt Is Nothing)
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(appt.Subject)
        sb.AppendLine("Start: " & appt.Start)
        sb.AppendLine("End: " & appt.End)
        Debug.WriteLine(sb.ToString())
        ' Find the next appointment
        appt = CType(calendarItems.FindNext(), Outlook.AppointmentItem)
    End While
    ' Restrict calendarItems with DASL query
    Dim restrictedItems As Outlook.Items = _
        calendarItems.Restrict(filter3)
    For Each apptItem As Outlook.AppointmentItem In restrictedItems
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(apptItem.Subject)
        sb.AppendLine("Start: " & apptItem.Start)
        sb.AppendLine("End: " & apptItem.End)
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    Next
End Sub
```


```csharp
private void SearchRecurringAppointments()
{
    Outlook.AppointmentItem appt = null;
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    // Set start value
    DateTime start =
        new DateTime(2006, 8, 9, 0, 0, 0);
    // Set end value
    DateTime end =
        new DateTime(2006, 12, 14, 0, 0, 0);
    // Initial restriction is Jet query for date range
    string filter1 = "[Start] >= '" +
        start.ToString("g")
        + "' AND [End] <= '" +
        end.ToString("g") + "'";
    Outlook.Items calendarItems = folder.Items.Restrict(filter1);
    calendarItems.IncludeRecurrences = true;
    calendarItems.Sort("[Start]", Type.Missing);
    // Must use 'like' comparison for Find/FindNext
    string filter2;
    filter2 = "@SQL="
        + "\"" + "urn:schemas:httpmail:subject" + "\""
        + " like '%Office%'";
    // Create DASL query for additional Restrict method
    string filter3;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " ci_startswith 'Office'";
    }
    else
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " like '%Office%'";
    }
    // Use Find and FindNext methods
    appt = calendarItems.Find(filter2)
        as Outlook.AppointmentItem;
    while (appt != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(appt.Subject);
        sb.AppendLine("Start: " + appt.Start);
        sb.AppendLine("End: " + appt.End);
        Debug.WriteLine(sb.ToString());
        // Find the next appointment
        appt = calendarItems.FindNext()
            as Outlook.AppointmentItem;
    }
    // Restrict calendarItems with DASL query
    Outlook.Items restrictedItems =
        calendarItems.Restrict(filter3);
    foreach (Outlook.AppointmentItem apptItem in restrictedItems)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(apptItem.Subject);
        sb.AppendLine("Start: " + apptItem.Start);
        sb.AppendLine("End: " + apptItem.End);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5add7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5add7-114">See also</span></span>

- [<span data-ttu-id="5add7-115">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="5add7-115">Search and filter</span></span>](search-and-filter.md)

