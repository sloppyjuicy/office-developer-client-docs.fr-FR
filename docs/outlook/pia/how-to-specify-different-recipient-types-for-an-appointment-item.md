---
title: Spécifier les différents types de destinataires d’un élément de rendez-vous
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c1f9e1d8e7b4c884853dda9b5c37cd7357d48b6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405685"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a><span data-ttu-id="f8c68-102">Spécifier les différents types de destinataires d’un élément de rendez-vous</span><span class="sxs-lookup"><span data-stu-id="f8c68-102">Uses the OlMeetingRecipientType enumeration to specify different recipient types for an appointment item.</span></span>

<span data-ttu-id="f8c68-103">Cet exemple indique comment utiliser l’énumération [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) pour spécifier différents types de destinataires pour un élément de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="f8c68-103">This example shows how to use the [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) enumeration to specify different recipient types for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="f8c68-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f8c68-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f8c68-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f8c68-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f8c68-106">Pour ajouter des destinataires à un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente une demande de réunion, utilisez l'énumération OlMeetingRecipientType de manière à spécifier si le destinataire du message est un participant obligatoire ou facultatif, ou encore une ressource (comme une salle ou un équipement).</span><span class="sxs-lookup"><span data-stu-id="f8c68-106">To add recipients to an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request, use the OlMeetingRecipientType enumeration to specify whether the recipient of the message is a required or optional attendee, or a resource (such as a room or equipment).</span></span>

<span data-ttu-id="f8c68-107">Dans l’exemple de code suivant, SetRecipientTypeForAppt crée un objet **AppointmentItem**, définit les propriétés de cet objet et ajoute les participants obligatoires et facultatifs.</span><span class="sxs-lookup"><span data-stu-id="f8c68-107">In the following code example,   creates an AppointmentItem object, sets properties for that object, and adds required and optional attendees.</span></span> <span data-ttu-id="f8c68-108">Cette propriété ajoute également une salle de conférence pour la réunion.</span><span class="sxs-lookup"><span data-stu-id="f8c68-108">It also adds a conference room for the meeting.</span></span> <span data-ttu-id="f8c68-109">La propriété [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) est définie sur [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)) pour indiquer que le rendez-vous est une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="f8c68-109">Note that the [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) property is set to [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)) , indicating that the appointment is a meeting request.</span></span>

<span data-ttu-id="f8c68-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f8c68-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f8c68-111">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="f8c68-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f8c68-112">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="f8c68-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
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

## <a name="see-also"></a><span data-ttu-id="f8c68-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c68-113">See also</span></span>

- [<span data-ttu-id="f8c68-114">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="f8c68-114">Appointments</span></span>](appointments.md)

