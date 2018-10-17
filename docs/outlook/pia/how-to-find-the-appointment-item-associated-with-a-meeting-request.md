---
title: Recherche de l’élément de rendez-vous associé à une demande de réunion
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 5fa3822206d86b976bcfa2360cecf3ef22602e96
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407498"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a><span data-ttu-id="e6a2c-102">Recherche de l’élément de rendez-vous associé à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="e6a2c-102">Find the appointment item associated with a meeting request</span></span>

<span data-ttu-id="e6a2c-103">Cet exemple montre comment utiliser la méthode [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) pour rechercher le rendez-vous qui est associé à une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-103">This example shows how to use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to find the appointment that is associated with a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="e6a2c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e6a2c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e6a2c-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e6a2c-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="e6a2c-106">Un objet [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) ne représente pas un rendez-vous mais un message contenant une demande d’ajout d’un rendez-vous au calendrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object does not represent an appointment, but a message that contains a request to add an appointment to the recipient's calendar.</span></span> <span data-ttu-id="e6a2c-107">Dans l’exemple de code suivant, MeetingRequestExample utilise la méthode [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) de l’objet **MeetingItem** sur chaque **MeetingItem** récupéré dans la Boîte de réception de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-107">In the following code example,   uses the GetAssociatedAppointment(Boolean) method of the MeetingItem object on each MeetingItem retrieved from the user's Inbox.</span></span> <span data-ttu-id="e6a2c-108">L’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) renvoyé est ensuite utilisé pour transmettre l’objet du rendez-vous aux écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6a2c-108">The returned [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is then used to write the subject of the appointment to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="e6a2c-109">Notez que l’argument **GetAssociatedAppointment** est défini sur **false** pour que le rendez-vous ne soit pas ajouté au calendrier de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-109">Note that **GetAssociatedAppointment** argument is set to **false** so that the appointment is not added to the user's calendar.</span></span>

<span data-ttu-id="e6a2c-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="e6a2c-111">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="e6a2c-112">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e6a2c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a2c-113">See also</span></span>

- [<span data-ttu-id="e6a2c-114">Demandes de réunion</span><span class="sxs-lookup"><span data-stu-id="e6a2c-114">Meeting Requests</span></span>](meeting-requests.md)

