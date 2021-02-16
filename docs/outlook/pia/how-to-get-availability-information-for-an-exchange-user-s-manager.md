---
title: Obtention des informations de disponibilité du responsable d’un utilisateur Exchange
TOCTitle: Get availability information for an Exchange user's manager
ms:assetid: b59dd875-50c2-4f24-ba91-24429abf1b72
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646996(v=office.15)
ms:contentKeyID: 55119849
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df3779a3b92368af75d152e662eedec1a30a97bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349482"
---
# <a name="get-availability-information-for-an-exchange-users-manager"></a>Obtention des informations de disponibilité du responsable d’un utilisateur Exchange

Cet exemple affiche le prochain créneau de 60 minutes disponible du responsable d’un utilisateur dans le calendrier.

## <a name="example"></a>Exemple

Cet exemple de code vérifie si l'utilisateur actif est un utilisateur Exchange. Si c'est le cas et si l'utilisateur a un responsable, il obtient les informations du responsable en appelant la méthode [GetExchangeUser](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) de l'objet [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) et la méthode [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) de l'objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) . Les informations du responsable sont contenues dans un objet **ExchangeUser** qui inclut le planning du responsable.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetManagerOpenInterval()
    Const slotLength As Integer = 60
    Dim addrEntry As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If addrEntry.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            Application.Session.CurrentUser. _
            AddressEntry.GetExchangeUser(). _
            GetExchangeUserManager()
        If Not (manager Is Nothing) Then
            Dim freeBusy As String = _
            manager.GetFreeBusy(DateTime.Now, slotLength, True)
            For i As Integer = 1 To freeBusy.Length - 1
                If (freeBusy.Substring(i, 1) = "0") Then
                    ' Get number of minutes into
                    ' the day for free interval
                    Dim busySlot As Double = (i - 1) * slotLength
                    ' Get an actual date/time
                    Dim dateBusySlot As DateTime = _
                        DateTime.Now.Date.AddMinutes(busySlot)
                    If (dateBusySlot.TimeOfDay >= _
                        DateTime.Parse("8:00 AM").TimeOfDay And _
                        dateBusySlot.TimeOfDay <= _
                        DateTime.Parse("5:00 PM").TimeOfDay And _
                        Not (dateBusySlot.DayOfWeek = _
                        DayOfWeek.Saturday Or _
                        dateBusySlot.DayOfWeek = DayOfWeek.Sunday))Then
                        Dim sb As StringBuilder = New StringBuilder()
                        sb.AppendLine( _
                            manager.Name & " first open interval:")
                        sb.AppendLine(dateBusySlot.ToString("f"))
                        Debug.WriteLine(sb.ToString())
                    End If
                End If
            Next
        End If
    End If
End Sub
```


```csharp
private void GetManagerOpenInterval()
{
    const int slotLength = 60;
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            string freeBusy = manager.GetFreeBusy(
                DateTime.Now, slotLength, true);
            for (int i = 1; i < freeBusy.Length; i++)
            {
                if (freeBusy.Substring(i, 1) == "0")
                {
                    // Get number of minutes into
                    // the day for free interval
                    double busySlot = (i - 1) * slotLength;
                    // Get an actual date/time
                    DateTime dateBusySlot =
                        DateTime.Now.Date.AddMinutes(busySlot);
                    if (dateBusySlot.TimeOfDay >=
                        DateTime.Parse("8:00 AM").TimeOfDay &
                        dateBusySlot.TimeOfDay <=
                        DateTime.Parse("5:00 PM").TimeOfDay &
                        !(dateBusySlot.DayOfWeek == 
                        DayOfWeek.Saturday |
                        dateBusySlot.DayOfWeek == DayOfWeek.Sunday))
                    {
                        StringBuilder sb = new StringBuilder();
                        sb.AppendLine(manager.Name
                            + " first open interval:");
                        sb.AppendLine(dateBusySlot.ToString("f"));
                        Debug.WriteLine(sb.ToString());
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)

