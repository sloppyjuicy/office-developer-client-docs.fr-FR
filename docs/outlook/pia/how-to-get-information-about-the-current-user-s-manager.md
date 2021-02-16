---
title: Obtention des informations du manager de l’utilisateur actuel
TOCTitle: Get information about the current user's manager
ms:assetid: 3a77fa51-e2e3-4544-849f-4267b1762270
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184603(v=office.15)
ms:contentKeyID: 55119846
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd5b49a2b1f1e494a494cf1bea4e105fa261e053
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349440"
---
# <a name="get-information-about-the-current-users-manager"></a><span data-ttu-id="6d7c4-102">Obtention des informations du manager de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="6d7c4-102">Get information about the current user's manager</span></span>

<span data-ttu-id="6d7c4-103">Cet exemple montre comment obtenir les informations (par exemple, le nom, la fonction et les numéros de téléphone) du manager de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-103">This example shows how to get information (such as name, job title, and phone numbers) about the current user’s manager.</span></span>

## <a name="example"></a><span data-ttu-id="6d7c4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6d7c4-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6d7c4-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6d7c4-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6d7c4-106">Dans la procédure suivante, GetManagerInfo appelle la méthode [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) pour obtenir un objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) qui représente le manager d’un **ExchangeUser** dans la hiérarchie organisationnelle.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-106">In the following procedure, GetManagerInfo calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to obtain an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object that represents the manager of an **ExchangeUser** in the organizational hierarchy.</span></span> <span data-ttu-id="6d7c4-107">La procédure teste si l’utilisateur connecté est en ligne pour vérifier que **GetExchangeUserManager** peut renvoyer un objet **ExchangeUser**.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-107">The procedure tests whether the logged-on user is online to ensure that **GetExchangeUserManager** can return an **ExchangeUser** object.</span></span> <span data-ttu-id="6d7c4-108">Si l’utilisateur n’est pas en ligne, **GetExchangeUserManager** renvoie une référence nulle.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-108">If the user is not online, **GetExchangeUserManager** will return a null reference.</span></span> <span data-ttu-id="6d7c4-109">GetManagerInfo écrit ensuite les informations relatives au manager dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d7c4-109">GetManagerInfo then writes manager information to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="6d7c4-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6d7c4-111">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6d7c4-112">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="6d7c4-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerInfo()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + manager.Name);
            sb.AppendLine("STMP address: "
                + manager.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + manager.JobTitle);
            sb.AppendLine("Department: "
                + manager.Department);
            sb.AppendLine("Location: "
                + manager.OfficeLocation);
            sb.AppendLine("Business phone: "
                + manager.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + manager.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="6d7c4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d7c4-113">See also</span></span>

- [<span data-ttu-id="6d7c4-114">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="6d7c4-114">Exchange users</span></span>](exchange-users.md)

