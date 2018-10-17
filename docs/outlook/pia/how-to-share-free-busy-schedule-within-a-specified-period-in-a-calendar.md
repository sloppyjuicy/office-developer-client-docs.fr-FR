---
title: Partage du planning de disponibilité pendant une période spécifiée dans un calendrier
TOCTitle: Share Free/Busy schedule within a specified period in a calendar
ms:assetid: 1d038f56-80dd-42fd-809b-f5b3a47cd5ee
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609503(v=office.15)
ms:contentKeyID: 55119824
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 359b328002b711930eab6c029474b3b39cbc184e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406189"
---
# <a name="share-freebusy-schedule-within-a-specified-period-in-a-calendar"></a><span data-ttu-id="542d2-102">Partage du planning de disponibilité pendant une période spécifiée dans un calendrier</span><span class="sxs-lookup"><span data-stu-id="542d2-102">Share Free/Busy schedule within a specified period in a calendar</span></span>

<span data-ttu-id="542d2-103">Cet exemple obtient les informations de disponibilité d’une semaine spécifiée à partir d’un calendrier et affiche les détails de disponibilité et d’objet à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="542d2-103">This example obtains the free/busy schedule within a specified week from a calendar and displays the free, busy, and subject details to the user.</span></span>

## <a name="example"></a><span data-ttu-id="542d2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="542d2-104">Example</span></span>

<span data-ttu-id="542d2-p101">Cet exemple de code utilise la méthode [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) de l'objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) pour obtenir un objet [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) pour le dossier Calendrier par défaut pour une période spécifique d'une semaine. Il appelle ensuite la méthode [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) sur l'objet **CalendarSharing** et affiche le message avec une charge utile iCalendar.</span><span class="sxs-lookup"><span data-stu-id="542d2-p101">This code sample uses the [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) method of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to obtain a [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object for the default Calendar folder for a specific one-week period. It then calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method on the **CalendarSharing** object and displays the message with an iCalendar payload.</span></span>

<span data-ttu-id="542d2-107">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="542d2-107">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="542d2-108">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="542d2-108">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="542d2-109">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="542d2-109">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub DemoCalendarSharing()
    ' Get instance of CalendarSharing object
    Dim calShare As Outlook.CalendarSharing = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar). _
        GetCalendarExporter()
    ' Free busy and subject details
    calShare.CalendarDetail = _
        Outlook.OlCalendarDetail.olFreeBusyAndSubject
    ' Set start and end dates
    calShare.StartDate = DateTime.Today
    calShare.EndDate = calShare.StartDate.AddDays(1)
    ' Call ForwardAsICal method
    Dim mail As Outlook.MailItem = _
        calShare.ForwardAsICal( _
        Outlook.OlCalendarMailFormat.olCalendarMailFormatDailySchedule)
    ' Add recipient
    mail.Recipients.Add("someone@example.com")
    mail.Recipients.ResolveAll()
    ' Set subject
    Dim CalName As String = _
    Application.Session.GetDefaultFolder( _
    Outlook.OlDefaultFolders.olFolderCalendar).Name
    mail.Subject = _
        Application.Session.CurrentUser.Name & _
        CalName.PadLeft(CalName.Length + 1)
    ' Display calendar sharing item
    mail.Display(False)
End Sub
```

```csharp
private void DemoCalendarSharing()
{
    // Get instance of CalendarSharing object
    Outlook.CalendarSharing calShare =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderCalendar).
        GetCalendarExporter();
    // Free busy and subject details
    calShare.CalendarDetail =
        Outlook.OlCalendarDetail.olFreeBusyAndSubject;
    // Set start and end dates
    calShare.StartDate = DateTime.Today;
    calShare.EndDate = calShare.StartDate.AddDays(1);
    // Call ForwardAsICal method
    Outlook.MailItem mail =
        calShare.ForwardAsICal(Outlook.OlCalendarMailFormat
        .olCalendarMailFormatDailySchedule);
    // Add recipient
    mail.Recipients.Add("someone@example.com");
    mail.Recipients.ResolveAll();
    // Set subject
    string CalName =
        Application.Session.GetDefaultFolder
    (Outlook.OlDefaultFolders.olFolderCalendar).Name;
    mail.Subject =
        Application.Session.CurrentUser.Name +
        CalName.PadLeft(CalName.Length + 1);
    // Display calendar sharing item
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="542d2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="542d2-110">See also</span></span>

- [<span data-ttu-id="542d2-111">Calendrier</span><span class="sxs-lookup"><span data-stu-id="542d2-111">Calendar</span></span>](calendar.md)

