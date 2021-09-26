---
title: Vérifier la réponse du responsable à une demande de réunion
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b2e55037cf4d1d2ae4d153472b8f58a6e184b9e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619357"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a>Vérifier la réponse du responsable à une demande de réunion

Cet exemple montre comment utiliser les méthodes [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) et [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) pour vérifier l'état de la réponse du responsable de l'utilisateur actuel à une demande de réunion.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Pour déterminer si un destinataire donné a accepté ou refusé une demande de réunion, utilisez la propriété [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) de l'objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) de la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associée à l'objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .

Dans l’exemple de code suivant, CheckManagerResponseStatus accepte un objet **AppointmentItem** en tant que paramètre. CheckManagerResponseStatus récupère l’objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) en appelant la méthode **GetExchangeUser** de l’utilisateur actuel. CheckManagerResponseStatus récupère ensuite l’objet **ExchangeUser** associé au responsable de l’utilisateur actuel en appelant la méthode **GetExchangeUserManager**. En utilisant la méthode [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), l’exemple vérifie ensuite si l’objet **Recipient** associé à l’objet **AppointmentItem** est le même que l’objet **ExchangeUser** qui représente le responsable de l’utilisateur. Si **CompareEntryIDs** renvoie **true**, le responsable de l’utilisateur se trouve dans la collection **Recipients** et CheckManagerResponseStatus renvoie l’élément **MeetingResponseStatus** du responsable. Si **CompareEntryIDs** renvoie **false**, CheckManagerResponseStatus renvoie une référence NULL.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)

