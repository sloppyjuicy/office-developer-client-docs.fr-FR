---
title: Accepter automatiquement une demande de réunion
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700331"
---
# <a name="automatically-accept-a-meeting-request"></a>Accepter automatiquement une demande de réunion

Cet exemple montre comment utiliser la méthode [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) pour accepter automatiquement une demande de réunion.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Un objet [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) représente une demande d’ajout de rendez-vous, représenté par un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), au calendrier d’un destinataire. Pour répondre à une demande de réunion, utilisez la méthode [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) afin d’obtenir l’objet **AppointmentItem** associé à la demande de réunion. Ensuite, utilisez la méthode [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) de l’objet **AppointmentItem** pour indiquer à l’organisateur de la réunion si elle a été acceptée, refusée ou ajoutée provisoirement au calendrier du destinataire. La méthode **Respond** accepte trois paramètres. 

Le paramètre *Response* indique si la réponse est Accepter, Refuser ou Tentative. Les paramètres fNoUI et fAdditionalTextDialog sont des valeurs **bool** qui déterminent respectivement si une réponse sera envoyée et si l’utilisateur peut ou non modifier la réponse. Dans l’exemple de code suivant, AutoAcceptMeetingRequests énumère chaque objet **MeetingItem** afin d’obtenir l’objet **AppointmentItem** associé. AutoAcceptMeetingRequests utilise ensuite la méthode **Respond** avec le paramètre *fNoUI* défini sur **true** pour indiquer qu’une réponse sera envoyée automatiquement afin d’accepter la demande de réunion.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Demandes de réunion](meeting-requests.md)

