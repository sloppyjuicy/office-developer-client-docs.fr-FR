---
title: Consultation de toutes les réponses à une demande de réunion
TOCTitle: Check all responses to a meeting request
ms:assetid: ebe10e5a-7f04-447a-bfc1-aa8a726cb0b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184650(v=office.15)
ms:contentKeyID: 55119881
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89f3aa7037659bb29346bb70338d535cbbc200b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709242"
---
# <a name="check-all-responses-to-a-meeting-request"></a><span data-ttu-id="4341a-102">Consultation de toutes les réponses à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="4341a-102">Check all responses to a meeting request</span></span>

<span data-ttu-id="4341a-103">Cet exemple montre comment vérifier le statut de la réponse de chaque destinataire à une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="4341a-103">This example shows how to check the status of each recipient’s response to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="4341a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="4341a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="4341a-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="4341a-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="4341a-106">Dans l’exemple de code suivant, CheckAttendeeStatus énumère la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) pour l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente une demande de réunion et examine la propriété [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) de chaque objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4341a-106">In the following code example, CheckAttendeeStatus enumerates the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request and examines the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object.</span></span> <span data-ttu-id="4341a-107">Chaque objet **Recipient** représente un destinataire de la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="4341a-107">Each **Recipient** object represents a recipient of the meeting request.</span></span> <span data-ttu-id="4341a-108">La valeur de la propriété **MeetingResponseStatus** peut être l'une des valeurs suivantes de l'énumération [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) :</span><span class="sxs-lookup"><span data-stu-id="4341a-108">The value of the **MeetingResponseStatus** property can be one of the following [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) enumeration values:</span></span>

- <span data-ttu-id="4341a-109">[olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4341a-109">[olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="4341a-110">[olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4341a-110">[olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="4341a-111">[olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4341a-111">[olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="4341a-112">[olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4341a-112">[olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="4341a-113">[olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4341a-113">[olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="4341a-114">[olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4341a-114">[olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>

<span data-ttu-id="4341a-115">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4341a-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4341a-116">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="4341a-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4341a-117">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="4341a-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CheckAttendeeStatus()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find("[Subject]='Sales Strategy FY2007'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            switch (recip.MeetingResponseStatus)
            {
                case Outlook.OlResponseStatus.olResponseAccepted:
                    Debug.WriteLine("Accepted: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseTentative:
                    Debug.WriteLine("Tentative: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseDeclined:
                    Debug.WriteLine("Declined: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseOrganized:
                    Debug.WriteLine("Organizer: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNone:
                    Debug.WriteLine("None: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNotResponded:
                    Debug.WriteLine("Not responded: " + recip.Name);
                    break;
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4341a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4341a-118">See also</span></span>

- [<span data-ttu-id="4341a-119">Demandes de réunion</span><span class="sxs-lookup"><span data-stu-id="4341a-119">Meeting requests</span></span>](meeting-requests.md)

