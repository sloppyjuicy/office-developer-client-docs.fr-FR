---
title: Créer une demande de réunion, ajouter des destinataires et spécifier un emplacement
TOCTitle: Create a meeting request, add recipients, and specify a location
ms:assetid: 3053c27e-34d9-440e-9b66-06de940c2813
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644964(v=office.15)
ms:contentKeyID: 55119873
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0f637d3d21f79ec538d10cf509fb09f5abf0b0ac
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723088"
---
# <a name="create-a-meeting-request-add-recipients-and-specify-a-location"></a>Créer une demande de réunion, ajouter des destinataires et spécifier un emplacement

Cet exemple crée un élément de rendez-vous comme demande de réunion, spécifie l'heure, les destinataires et l'emplacement de la réunion, et affiche un rendez-vous dans un inspecteur.

## <a name="example"></a>Exemple

Dans Outlook, une demande de réunion est un [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Pour définir un élément de rendez-vous en tant que demande de réunion, vous devez définir la propriété [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) sur **olMeeting**. Utilisez la propriété [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) de l'objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) pour spécifier si le participant à la réunion est facultatif ou si un destinataire est en fait une ressource de réunion plutôt qu'un participant.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SetRecipientTypeForAppt()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    appt.Subject = "Customer Review"
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting
    appt.Location = "36/2021"
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM")
    appt.End = DateTime.Parse("10/20/2006 11:00 AM")
    Dim recipRequired As Outlook.Recipient = _
        appt.Recipients.Add("Ryan Gregg")
    recipRequired.Type = _
        Outlook.OlMeetingRecipientType.olRequired
    Dim recipOptional As Outlook.Recipient = _
        appt.Recipients.Add("Peter Allenspach")
    recipOptional.Type = _
        Outlook.OlMeetingRecipientType.olOptional
    Dim recipConf As Outlook.Recipient = _
        appt.Recipients.Add("Conf Room 36/2021 (14) AV")
    recipConf.Type = _
        Outlook.OlMeetingRecipientType.olResource
    appt.Recipients.ResolveAll()
    appt.Display(False)
End Sub
```


```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
       appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>Voir aussi

- [Demandes de réunion](meeting-requests.md)

