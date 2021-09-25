---
title: Enregistrement d’un calendrier sur disque
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 40b6843463bd7708d27d14da831f097a1b3a4031
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590633"
---
# <a name="save-a-calendar-to-disk"></a>Enregistrement d’un calendrier sur disque

Cet exemple montre comment enregistrer un calendrier entier sur le disque au format de fichier iCalendar (.ics).

## <a name="example"></a>Exemple

Cet exemple de code utilise l'objet [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) qui prend en charge l'enregistrement d'un calendrier entier ou d'une plage de rendez-vous du calendrier sur le disque. Outlook optimise automatiquement un fichier .ics afin que les rendez-vous périodiques n'y soient pas enregistrés en tant que rendez-vous individuels. Selon la taille du calendrier enregistré, l'enregistrement sur disque peut être relativement long. Pendant l'enregistrement du calendrier, la fenêtre Outlook ne répond plus à l'utilisateur.

L'exemple de code commence par appeler la méthode [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) sur le dossier Calendrier par défaut pour obtenir un objet **CalendarSharing**. Il définit ensuite les propriétés de l'objet **CalendarSharing** afin de spécifier les critères de l'exportation, comme le fait que le calendrier entier doit être enregistré et inclure les détails des rendez-vous marqués comme « privés ».

Pour enregistrer les informations au format de fichier .ics, l’exemple de code appelle la méthode [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) de l’objet **CalendarSharing**.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a>Voir aussi

- [Calendar](calendar.md)

