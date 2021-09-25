---
title: Filtrage des rendez-vous périodiques et recherche d’une chaîne dans l’objet
TOCTitle: Filter recurring appointments and search for a string in the subject
ms:assetid: 997186aa-5264-4b19-bed6-51c38831c03d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611267(v=office.15)
ms:contentKeyID: 55119891
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 70901903e2c2a24add9b1e43c4e4ae94ce33b043
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560549"
---
# <a name="filter-recurring-appointments-and-search-for-a-string-in-the-subject"></a>Filtrage des rendez-vous périodiques et recherche d’une chaîne dans l’objet

Cet exemple filtre les rendez-vous périodiques compris dans une plage de dates dans un dossier Calendrier, puis recherche la chaîne « office » dans l’objet de ces rendez-vous de deux manières différentes.

## <a name="example"></a>Exemple

Pour filtrer des rendez-vous périodiques, cet exemple de code utilise la collection [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) à la place de l’objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), car l’objet **Table** renvoie uniquement les rendez-vous principaux de la collection et n’inclut pas les éléments périodiques du dossier. Pour inclure les rendez-vous périodiques pendant l’appel de la méthode [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) ou [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)), l’exemple de code définit la propriété [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) de la collection **Items**, puis trie les rendez-vous du dossier selon la date indiquée dans la propriété [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)). Il utilise ensuite une requête Jet pour indiquer les dates de début et de fin des périodicités.

Après avoir obtenu une collection d’éléments de rendez-vous périodiques **Items** compris dans la plage de dates spécifiée, l’exemple de code effectue deux autres recherches à l’aide des requêtes DASL (DAV Searching and Locating). La première recherche utilise les méthodes **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\))et le mot clé **like** pour rechercher tous les éléments dont la sous-chaîne « office » figure dans l’objet. La deuxième recherche utilise la méthode **Items.Restrict** et le mot clé **ci\_startswith** pour rechercher tous les éléments dont l’objet commence par « office ».

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

