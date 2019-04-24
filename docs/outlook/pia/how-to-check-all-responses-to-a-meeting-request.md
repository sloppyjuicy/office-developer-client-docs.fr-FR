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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359716"
---
# <a name="check-all-responses-to-a-meeting-request"></a>Consultation de toutes les réponses à une demande de réunion

Cet exemple montre comment vérifier le statut de la réponse de chaque destinataire à une demande de réunion.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, CheckAttendeeStatus énumère la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) pour l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente une demande de réunion et examine la propriété [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) de chaque objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)). Chaque objet **Recipient** représente un destinataire de la demande de réunion. La valeur de la propriété **MeetingResponseStatus** peut être l'une des valeurs suivantes de l'énumération [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) :

- [olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Demandes de réunion](meeting-requests.md)

