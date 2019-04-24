---
title: Obtention des informations des collaborateurs directs du manager de l’utilisateur actuel
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d49e96138d8cd2d857c49cc293258e1493afc747
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349433"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a><span data-ttu-id="5aaae-102">Obtention des informations des collaborateurs directs du responsable de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="5aaae-102">Get information about direct reports of the current user's manager</span></span>

<span data-ttu-id="5aaae-103">Cet exemple obtient les subordonnés du responsable de l’utilisateur actif, le cas échéant, puis affiche des informations sur chaque subordonné du responsable.</span><span class="sxs-lookup"><span data-stu-id="5aaae-103">This example gets the direct reports of the current user’s manager, if any, and then displays information about each of the manager’s direct reports.</span></span>

## <a name="example"></a><span data-ttu-id="5aaae-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5aaae-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5aaae-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5aaae-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="5aaae-106">Dans l’exemple suivant, la procédure GetManagerDirectReports appelle la méthode [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) pour obtenir le responsable de l’utilisateur, représenté par un objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5aaae-106">In the following example, the GetManagerDirectReports procedure calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to get the user’s manager, represented by an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="5aaae-107">Si l’utilisateur actif a un responsable, la méthode [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) est appelée pour renvoyer une collection [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) qui représente les entrées d’adresse de tous les collaborateurs directs du responsable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5aaae-107">If the current user has a manager, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) is called to return an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that represents the address entries for all the direct reports of user’s manager.</span></span> <span data-ttu-id="5aaae-108">Si le responsable n’a aucun collaborateur direct, **GetDirectReports** renvoie une collection **AddressEntries** qui a un décompte de zéro.</span><span class="sxs-lookup"><span data-stu-id="5aaae-108">If the manager has no direct reports, **GetDirectReports** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="5aaae-109">Une fois les collaborateurs directs du responsable obtenus, GetManagerDirectReports écrit des informations sur chacun des collaborateurs directs du responsable dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="5aaae-109">Once the manager’s direct reports are obtained, GetManagerDirectReports writes information about each of the manager’s direct reports to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="5aaae-110">L’utilisateur doit être en ligne pour que cette méthode renvoie une collection **AddressEntries**. Sinon, **GetDirectReports** renvoie une référence Null.</span><span class="sxs-lookup"><span data-stu-id="5aaae-110">The signed-in user must be online for this method to return an **AddressEntries** collection; otherwise, **GetDirectReports** returns a null reference.</span></span> <span data-ttu-id="5aaae-111">Pour le code de production, vous devez tester que l’utilisateur est hors connexion à l’aide de la propriété [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) ou [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) pour plusieurs scénarios Exchange.</span><span class="sxs-lookup"><span data-stu-id="5aaae-111">For production code, you must test for the user being offline by using the [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) property, or the [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) property for multiple Exchange scenarios.</span></span>

<span data-ttu-id="5aaae-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5aaae-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5aaae-113">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="5aaae-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5aaae-114">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="5aaae-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5aaae-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aaae-115">See also</span></span>

- [<span data-ttu-id="5aaae-116">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="5aaae-116">Exchange users</span></span>](exchange-users.md)

