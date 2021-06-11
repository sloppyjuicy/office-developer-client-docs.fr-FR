---
title: Obtention des informations de plusieurs comptes
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d065761b9296f1c0eb3043e9b9778e438790f94e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349412"
---
# <a name="get-information-about-multiple-accounts"></a><span data-ttu-id="c7805-102">Obtention des informations de plusieurs comptes</span><span class="sxs-lookup"><span data-stu-id="c7805-102">Get information about multiple accounts</span></span>

<span data-ttu-id="c7805-103">Outlook prend en charge un profil qui contient un ou plusieurs comptes connectés à un ordinateur Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c7805-103">Outlook supports a profile that contains one or more accounts that are connected to an Exchange Server.</span></span> <span data-ttu-id="c7805-104">Cet exemple montre comment obtenir et afficher des informations diverses sur chaque compte dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="c7805-104">This example shows how to obtain and display miscellaneous information about each account in the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="c7805-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7805-105">Example</span></span>

<span data-ttu-id="c7805-p102">La méthode suivante, EnumerateAccounts, affiche le nom du compte, le nom d’utilisateur et l’adresse SMTP (Simple Mail Transfer Protocol) pour chaque compte défini dans le profil actif. Si le compte est connecté à un serveur Exchange, EnumerateAccounts affiche le nom du serveur Exchange et les informations de version. Et si le compte réside dans une banque de remise, EnumerateAccounts affiche le nom de la banque de remise par défaut pour le compte.</span><span class="sxs-lookup"><span data-stu-id="c7805-p102">The following method, EnumerateAccounts, displays the account name, user name, and Simple Mail Transfer Protocol (SMTP) address for each account that is defined in the current profile. If the account is connected to an Exchange server, EnumerateAccounts displays the Exchange server name and version information. And if the account resides on a delivery store, EnumerateAccounts displays the name of the default delivery store for the account.</span></span>

<span data-ttu-id="c7805-109">EnumerateAccounts accède à la plupart de ces informations à partir de l’objet [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), hormis lorsque l’objet **Account** ne contient pas d’informations relatives au nom d’utilisateur et à l’adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="c7805-109">EnumerateAccounts accesses most of this information from the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object, except when the **Account** object does not contain information about the user name and SMTP address.</span></span> <span data-ttu-id="c7805-110">Dans ce cas, EnumerateAccounts utilise les objets [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) et [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c7805-110">In that case, EnumerateAccounts uses the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) and [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) objects.</span></span> 

<span data-ttu-id="c7805-111">EnumerateAccounts obtient l’objet **AddressEntry** en utilisant la propriété [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) de l’objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) obtenu à partir de la propriété [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c7805-111">EnumerateAccounts obtains the **AddressEntry** object by using the [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object obtained from the [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)) property.</span></span> <span data-ttu-id="c7805-112">EnumerateAccounts obtient l’objet **ExchangeUser** en utilisant la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) de l’objet **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="c7805-112">EnumerateAccounts obtains the **ExchangeUser** object by using the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method of the **AddressEntry** object.</span></span> 

<span data-ttu-id="c7805-113">Voici l’algorithme qui permet d’obtenir des informations diverses à l’aide des objets Account, AddressEntry et ExchangeUser :</span><span class="sxs-lookup"><span data-stu-id="c7805-113">The following is the algorithm to obtain various information by using the Account, AddressEntry, and ExchangeUser objects:</span></span>

- <span data-ttu-id="c7805-114">Si l'objet **Account** contient des informations relatives au nom d'utilisateur et à l'adresse SMTP, utiliser l'objet **Account** pour afficher le nom du compte, le nom d'utilisateur et l'adresse SMTP, ainsi que les informations de version et le nom du serveur Exchange s'il s'agit d'un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7805-114">If the **Account** object contains information about the user name and SMTP address, use the **Account** object to display the account name, user name, SMTP address, and Exchange server name and version information if the account is an Exchange account.</span></span>

- <span data-ttu-id="c7805-115">Si l'objet **Account** ne contient pas d'informations relatives au nom d'utilisateur et à l'adresse SMTP, procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="c7805-115">If the **Account** object does not contain information about the user name and SMTP address, proceed as follows:</span></span>
    
  - <span data-ttu-id="c7805-116">Si le compte n'est pas un compte Exchange, utiliser l'objet **AddressEntry** pour afficher le nom d'utilisateur et l'adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="c7805-116">If the account is not an Exchange account, use the **AddressEntry** object to display the user name and SMTP address.</span></span>
    
  - <span data-ttu-id="c7805-117">Si le compte est un compte Exchange, procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="c7805-117">If the account is an Exchange account, proceed as follows:</span></span>
        
    1.  <span data-ttu-id="c7805-118">Utiliser l'objet **Account** pour afficher le nom du compte, le nom du serveur Exchange et les informations sur la version Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7805-118">Use the **Account** object to display the account name, Exchange server name, and Exchange version information.</span></span>
        
    2.  <span data-ttu-id="c7805-119">Utilisez l’objet **ExchangeUser** pour afficher le nom d’utilisateur et l’adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="c7805-119">Use the **ExchangeUser** object to display the user name and SMTP address.</span></span>

<span data-ttu-id="c7805-120">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c7805-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c7805-121">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="c7805-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c7805-122">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="c7805-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAccounts()
{
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        try
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Account: " + account.DisplayName);
            if (string.IsNullOrEmpty(account.SmtpAddress)
                || string.IsNullOrEmpty(account.UserName))
            {
                Outlook.AddressEntry oAE =
                    account.CurrentUser.AddressEntry
                    as Outlook.AddressEntry;
                if (oAE.Type == "EX")
                {
                    Outlook.ExchangeUser oEU =
                        oAE.GetExchangeUser()
                        as Outlook.ExchangeUser;
                    sb.AppendLine("UserName: " +
                        oEU.Name);
                    sb.AppendLine("SMTP: " +
                        oEU.PrimarySmtpAddress);
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
                else
                {
                    sb.AppendLine("UserName: " +
                        oAE.Name);
                    sb.AppendLine("SMTP: " +
                        oAE.Address);
                }
            }
            else
            {
                sb.AppendLine("UserName: " +
                    account.UserName);
                sb.AppendLine("SMTP: " +
                    account.SmtpAddress);
                if(account.AccountType == 
                    Outlook.OlAccountType.olExchange)
                {
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
            }
            if(account.DeliveryStore !=null)
            {
                sb.AppendLine("Delivery Store: " +
                    account.DeliveryStore.DisplayName);
            }
            sb.AppendLine("---------------------------------");
            Debug.Write(sb.ToString());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c7805-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7805-123">See also</span></span>

- [<span data-ttu-id="c7805-124">Comptes</span><span class="sxs-lookup"><span data-stu-id="c7805-124">Accounts</span></span>](accounts.md)

