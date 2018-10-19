---
title: Obtention des informations de toutes les listes de distribution dont l’utilisateur actuel est membre
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f98d7a338866624e67d745e66a66e864fb9bbf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406763"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="dd112-102">Obtention des informations de toutes les listes de distribution dont l’utilisateur actuel est membre</span><span class="sxs-lookup"><span data-stu-id="dd112-102">Get information about all distribution lists of which the current user is a member</span></span>

<span data-ttu-id="dd112-103">Cet exemple utilise la méthode [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) pour obtenir des informations sur toutes les listes de distribution dont l’utilisateur actuel est membre.</span><span class="sxs-lookup"><span data-stu-id="dd112-103">This example uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="dd112-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="dd112-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="dd112-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="dd112-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="dd112-106">Dans l’exemple de code suivant, GetCurrentUserMembership appelle la méthode **GetMemberOfList** afin d’obtenir une collection [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) pour toutes les listes de distribution dont l’utilisateur Exchange est membre.</span><span class="sxs-lookup"><span data-stu-id="dd112-106">In the following example,   calls the GetMemberOfList method to get an AddressEntries collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="dd112-107">Si l’utilisateur n’est pas membre d’une liste de distribution, **GetMemberOfList** renvoie une collection **AddressEntries** qui a un décompte de zéro.</span><span class="sxs-lookup"><span data-stu-id="dd112-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="dd112-108">L’utilisateur doit être en ligne pour que **GetMemberOfList** renvoie une collection **AddressEntries**. Sinon, **GetMemberOfList** renvoie une référence Null.</span><span class="sxs-lookup"><span data-stu-id="dd112-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="dd112-109">GetCurrentUserMembership utilise la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), qui renvoie l’objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) actuel pour tester si l’utilisateur est en ligne.</span><span class="sxs-lookup"><span data-stu-id="dd112-109"> uses the GetExchangeUser() method, which returns the current ExchangeUser object, to test whether the user is online.</span></span> <span data-ttu-id="dd112-110">Une fois les entrées d’adresse obtenues, l’exemple écrit des informations sur chacune des listes de distribution de l’utilisateur dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd112-110">Once the address entries are obtained, the example writes information about each of the user's distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="dd112-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dd112-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="dd112-112">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="dd112-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="dd112-113">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="dd112-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dd112-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd112-114">See also</span></span>

- [<span data-ttu-id="dd112-115">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="dd112-115">Exchange Users</span></span>](exchange-users.md)

