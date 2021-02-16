---
title: Vérifier la réponse du responsable à une demande de réunion
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba54ba740182eaffc92a0e1932a6fbed1d3804c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359709"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a><span data-ttu-id="e4ffc-102">Vérifier la réponse du responsable à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="e4ffc-102">Check a manager's response to a meeting request</span></span>

<span data-ttu-id="e4ffc-103">Cet exemple montre comment utiliser les méthodes [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) et [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) pour vérifier l'état de la réponse du responsable de l'utilisateur actuel à une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-103">This example illustrates how to use the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="e4ffc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4ffc-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e4ffc-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e4ffc-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e4ffc-106">Pour déterminer si un destinataire donné a accepté ou refusé une demande de réunion, utilisez la propriété [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) de l'objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) de la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associée à l'objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="e4ffc-106">To determine whether a given recipient has accepted or declined a requested meeting, use the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object from the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection associated with the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="e4ffc-107">Dans l’exemple de code suivant, CheckManagerResponseStatus accepte un objet **AppointmentItem** en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-107">In the following code example, CheckManagerResponseStatus takes in an **AppointmentItem** object as a parameter.</span></span> <span data-ttu-id="e4ffc-108">CheckManagerResponseStatus récupère l’objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) en appelant la méthode **GetExchangeUser** de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-108">CheckManagerResponseStatus gets the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object by calling the **GetExchangeUser** method on the current user.</span></span> <span data-ttu-id="e4ffc-109">CheckManagerResponseStatus récupère ensuite l’objet **ExchangeUser** associé au responsable de l’utilisateur actuel en appelant la méthode **GetExchangeUserManager**.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-109">CheckManagerResponseStatus then gets the **ExchangeUser** object that is associated with the current user’s manager by calling the **GetExchangeUserManager** method.</span></span> <span data-ttu-id="e4ffc-110">En utilisant la méthode [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), l’exemple vérifie ensuite si l’objet **Recipient** associé à l’objet **AppointmentItem** est le même que l’objet **ExchangeUser** qui représente le responsable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-110">By using the [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object, the example then checks whether the **Recipient** object associated with the **AppointmentItem** object is the same as the **ExchangeUser** object that represents the user’s manager.</span></span> <span data-ttu-id="e4ffc-111">Si **CompareEntryIDs** renvoie **true**, le responsable de l’utilisateur se trouve dans la collection **Recipients** et CheckManagerResponseStatus renvoie l’élément **MeetingResponseStatus** du responsable.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-111">If **CompareEntryIDs** returns **true**, the user’s manager is found in the **Recipients** collection, and CheckManagerResponseStatus returns the manager’s **MeetingResponseStatus**.</span></span> <span data-ttu-id="e4ffc-112">Si **CompareEntryIDs** renvoie **false**, CheckManagerResponseStatus renvoie une référence NULL.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-112">If **CompareEntryIDs** returns **false**, CheckManagerResponseStatus returns a null reference.</span></span>

<span data-ttu-id="e4ffc-113">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e4ffc-114">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e4ffc-115">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="e4ffc-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e4ffc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4ffc-116">See also</span></span>

- [<span data-ttu-id="e4ffc-117">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="e4ffc-117">Exchange users</span></span>](exchange-users.md)

