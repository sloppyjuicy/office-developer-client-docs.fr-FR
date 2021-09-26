---
title: Obtention de l’organisateur d’une réunion
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 321cf15e0f1144518d526c3897863e9bf3d681dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583148"
---
# <a name="get-the-organizer-of-a-meeting"></a>Obtention de l’organisateur d’une réunion

Cet exemple montre comment renvoyer, par programme, l’organisateur d’une réunion.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, GetMeetingOrganizer accepte un paramètre de type [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente une réunion, et utilise l’objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) et la méthode [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) pour obtenir l’ID [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) de l’objet **AppointmentItem**. Une fois l’ID **EntryID** obtenu, l’exemple utilise la méthode [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) pour renvoyer l’objet [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) qui représente l’organisateur de la réunion.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"http://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Demandes de réunion](meeting-requests.md)

