---
title: Partage des informations de calendrier par e-mail
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48b299ad4d3afe5c0c9aaa05f5d8af3b92bf655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332078"
---
# <a name="share-calendar-information-through-email"></a><span data-ttu-id="7b4e1-102">Partage des informations de calendrier par e-mail</span><span class="sxs-lookup"><span data-stu-id="7b4e1-102">Share calendar information through email</span></span>

<span data-ttu-id="7b4e1-103">Cet exemple montre comment partager des informations d’un calendrier par courrier électronique au format iCalendar.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-103">This example shows how to share information from a calendar by email in the iCalendar format.</span></span>

## <a name="example"></a><span data-ttu-id="7b4e1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7b4e1-104">Example</span></span>

<span data-ttu-id="7b4e1-p101">Le format iCalendar vous permet d'envoyer des éléments à d'autres clients Outlook ou non-Outlook par le biais de protocoles et formats de messagerie Internet standard. L'exemple de code utilise l'objet [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) qui prend en charge l'exportation d'informations d'un dossier de calendrier au format iCalendar.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-p101">The iCalendar format allows you to send items to other Outlook or non-Outlook clients via standard Internet mail formats and protocols. The code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports exporting information from a calendar folder to the iCalendar format.</span></span>

<span data-ttu-id="7b4e1-p102">L'exemple de code appelle tout d'abord [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) sur le dossier Calendrier par défaut afin d'obtenir un objet **CalendarSharing**. Il définit ensuite les propriétés de l'objet **CalendarSharing** pour spécifier les critères d'exportation, tels que la plage de dates des informations de calendrier, s'il faut inclure les pièces jointes, et les détails des rendez-vous marqués comme « privés ».</span><span class="sxs-lookup"><span data-stu-id="7b4e1-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as the date range of calendar information, whether to include attachments, and details of appointments that are marked "private."</span></span>

<span data-ttu-id="7b4e1-109">Pour envoyer les informations de calendrier par messagerie, l’exemple de code appelle la méthode [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) de l’objet **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-109">To send the calendar information by email, the code sample calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="7b4e1-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7b4e1-111">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7b4e1-112">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub SendNextWeekToAddress(ByVal sendToAddresses As String)
    If String.IsNullOrEmpty(sendToAddresses) Then
        Throw New ArgumentException( _
            "Parameter must contain a value.", "sendToAddress")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = False
    exporter.RestrictToWorkingHours = False
    exporter.StartDate = DateTime.Today.Date
    exporter.EndDate = DateTime.Today.Date.AddDays(7)

    '' Create a new mail item
    Dim calendarMail As Outlook.MailItem = exporter.ForwardAsICal _
        (Outlook.OlCalendarMailFormat. _
        olCalendarMailFormatDailySchedule)
    calendarMail.To = sendToAddresses
    calendarMail.Send()
    calendarMail.Display()
End Sub
```

```csharp
private void SendNextWeekToAddress(string sendToAddresses)
{
    if (string.IsNullOrEmpty(sendToAddresses))
        throw new ArgumentException(
        "sendToAddress","Parameter must contain a value.");
    Outlook.Folder calendar = 
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = false;
    exporter.RestrictToWorkingHours = false;
    exporter.StartDate = DateTime.Today.Date;
    exporter.EndDate = DateTime.Today.Date.AddDays(7);

    // Create a new mail item
    Outlook.MailItem calendarMail = 
        exporter.ForwardAsICal(Outlook.OlCalendarMailFormat.
        olCalendarMailFormatDailySchedule);
    calendarMail.To = sendToAddresses;
    ((Outlook.MailItemClass)calendarMail).Send();
    ((Outlook.MailItemClass)calendarMail).Display(Type.Missing);
}
```

## <a name="see-also"></a><span data-ttu-id="7b4e1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b4e1-113">See also</span></span>

- [<span data-ttu-id="7b4e1-114">Calendar</span><span class="sxs-lookup"><span data-stu-id="7b4e1-114">Calendar</span></span>](calendar.md)

