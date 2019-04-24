---
title: Validation automatique d’une demande de réunion
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359702"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="c2a3d-102">Accepter automatiquement une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="c2a3d-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="c2a3d-103">Cet exemple montre comment utiliser la méthode [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) pour accepter automatiquement une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-103">This example shows how to use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="c2a3d-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2a3d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c2a3d-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c2a3d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="c2a3d-106">Un objet [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) représente une demande d’ajout de rendez-vous, représenté par un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), au calendrier d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="c2a3d-107">Pour répondre à une demande de réunion, utilisez la méthode [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) afin d’obtenir l’objet **AppointmentItem** associé à la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="c2a3d-108">Ensuite, utilisez la méthode [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) de l’objet **AppointmentItem** pour indiquer à l’organisateur de la réunion si elle a été acceptée, refusée ou ajoutée provisoirement au calendrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="c2a3d-109">La méthode **Respond** accepte trois paramètres.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-109">The **Respond** method accepts three parameters.</span></span> 

<span data-ttu-id="c2a3d-110">Le paramètre *Response* indique si la réponse est Accepter, Refuser ou Tentative.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="c2a3d-111">Les paramètres fNoUI et fAdditionalTextDialog sont des valeurs **bool** qui déterminent respectivement si une réponse sera envoyée et si l’utilisateur peut ou non modifier la réponse.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="c2a3d-112">Dans l’exemple de code suivant, AutoAcceptMeetingRequests énumère chaque objet **MeetingItem** afin d’obtenir l’objet **AppointmentItem** associé.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="c2a3d-113">AutoAcceptMeetingRequests utilise ensuite la méthode **Respond** avec le paramètre *fNoUI* défini sur **true** pour indiquer qu’une réponse sera envoyée automatiquement afin d’accepter la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="c2a3d-114">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c2a3d-115">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c2a3d-116">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="c2a3d-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c2a3d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2a3d-117">See also</span></span>

- [<span data-ttu-id="c2a3d-118">Demandes de réunion</span><span class="sxs-lookup"><span data-stu-id="c2a3d-118">Meeting requests</span></span>](meeting-requests.md)

