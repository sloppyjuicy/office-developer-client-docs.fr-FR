---
title: Enregistrement d’un calendrier sur disque
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361046"
---
# <a name="save-a-calendar-to-disk"></a><span data-ttu-id="503b6-102">Enregistrement d’un calendrier sur disque</span><span class="sxs-lookup"><span data-stu-id="503b6-102">Save a calendar to disk</span></span>

<span data-ttu-id="503b6-103">Cet exemple montre comment enregistrer un calendrier entier sur le disque au format de fichier iCalendar (.ics).</span><span class="sxs-lookup"><span data-stu-id="503b6-103">This example shows how to save an entire calendar to disk in the iCalendar (.ics) file format.</span></span>

## <a name="example"></a><span data-ttu-id="503b6-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="503b6-104">Example</span></span>

<span data-ttu-id="503b6-p101">Cet exemple de code utilise l'objet [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) qui prend en charge l'enregistrement d'un calendrier entier ou d'une plage de rendez-vous du calendrier sur le disque. Outlook optimise automatiquement un fichier .ics afin que les rendez-vous périodiques n'y soient pas enregistrés en tant que rendez-vous individuels. Selon la taille du calendrier enregistré, l'enregistrement sur disque peut être relativement long. Pendant l'enregistrement du calendrier, la fenêtre Outlook ne répond plus à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="503b6-p101">This code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports saving a whole calendar or a range of appointments from the calendar to disk. Outlook automatically optimizes an .ics file so that recurring appointments are not saved as individual appointments in the .ics file. Depending on the size of the calendar being saved, saving a calendar to disk can take a significant amount of time. While saving the calendar, the Outlook window appears unresponsive to the user.</span></span>

<span data-ttu-id="503b6-p102">L'exemple de code commence par appeler la méthode [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) sur le dossier Calendrier par défaut pour obtenir un objet **CalendarSharing**. Il définit ensuite les propriétés de l'objet **CalendarSharing** afin de spécifier les critères de l'exportation, comme le fait que le calendrier entier doit être enregistré et inclure les détails des rendez-vous marqués comme « privés ».</span><span class="sxs-lookup"><span data-stu-id="503b6-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as whether to save the entire calendar and include details of appointments that are marked "private".</span></span>

<span data-ttu-id="503b6-111">Pour enregistrer les informations au format de fichier .ics, l’exemple de code appelle la méthode [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) de l’objet **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="503b6-111">To save the calendar information in .ics file format, the code sample calls the [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="503b6-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="503b6-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="503b6-113">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="503b6-113">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="503b6-114">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="503b6-114">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="503b6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="503b6-115">See also</span></span>

- [<span data-ttu-id="503b6-116">Calendar</span><span class="sxs-lookup"><span data-stu-id="503b6-116">Calendar</span></span>](calendar.md)

