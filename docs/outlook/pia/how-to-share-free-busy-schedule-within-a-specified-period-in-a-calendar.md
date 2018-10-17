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
# <a name="share-freebusy-schedule-within-a-specified-period-in-a-calendar"></a>Partage du planning de disponibilité pendant une période spécifiée dans un calendrier

Cet exemple obtient les informations de disponibilité d’une semaine spécifiée à partir d’un calendrier et affiche les détails de disponibilité et d’objet à l’utilisateur.

## <a name="example"></a>Exemple

Cet exemple de code utilise la méthode [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) de l'objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) pour obtenir un objet [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) pour le dossier Calendrier par défaut pour une période spécifique d'une semaine. Il appelle ensuite la méthode [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) sur l'objet **CalendarSharing** et affiche le message avec une charge utile iCalendar.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Calendrier](calendar.md)

