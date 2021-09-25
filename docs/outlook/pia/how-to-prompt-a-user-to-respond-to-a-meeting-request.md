---
title: Invitation d’un utilisateur pour répondre à une demande de réunion
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0c5a5b3d1ccaf70c6adc57f7259b6d6a2714f009
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560479"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a>Invitation d’un utilisateur pour répondre à une demande de réunion

Cet exemple montre comment inviter l'utilisateur à répondre à une demande de réunion et comment lui permettre de modifier la réponse avant de l'envoyer.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

La méthode [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) de l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) est utilisée pour indiquer à l’organisateur de la réunion si la réunion a été acceptée, refusée ou s’il y a eu une tentative d’ajout au calendrier du destinataire. À l'aide de la méthode **Respond**, vous pouvez indiquer si vous souhaitez envoyer automatiquement la notification, ou si vous voulez permettre à l'utilisateur de modifier la réponse avant de l'envoyer. La méthode **Respond** accepte trois paramètres. Le paramètre *Response* indique si la réponse est Accepter, Refuser ou Tentative. Les paramètres *fNoUI* et *fAdditionalTextDialog* sont des valeurs de type **bool** qui indiquent respectivement si la réponse sera envoyée à l’organisateur et si l’utilisateur peut modifier le corps de la réponse avant de l’envoyer. 

Dans l’exemple de code suivant, PromptUserMeetingRequest énumère les objets [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) pour obtenir les objets **AppointmentItem** associés, puis appelle la méthode **Respond** dont le paramètre *fNoUI* est défini sur **false** et le paramètre *fAdditionalTextDialog* est défini sur **true**. Ainsi, l’utilisateur peut choisir d’envoyer une réponse et de modifier le corps de la réponse avant de l’envoyer.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
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
                false, true);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Demandes de réunion](meeting-requests.md)

