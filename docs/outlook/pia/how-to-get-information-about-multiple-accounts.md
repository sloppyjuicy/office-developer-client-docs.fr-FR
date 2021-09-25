---
title: Obtention des informations de plusieurs comptes
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 179cf1e4fb54098c40ce2b080b4569b9392de90b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590652"
---
# <a name="get-information-about-multiple-accounts"></a>Obtention des informations de plusieurs comptes

Outlook prend en charge un profil qui contient un ou plusieurs comptes connectés à un ordinateur Exchange Server. Cet exemple montre comment obtenir et afficher des informations diverses sur chaque compte dans le profil actuel.

## <a name="example"></a>Exemple

La méthode suivante, EnumerateAccounts, affiche le nom du compte, le nom d’utilisateur et l’adresse SMTP (Simple Mail Transfer Protocol) pour chaque compte défini dans le profil actif. Si le compte est connecté à un serveur Exchange, EnumerateAccounts affiche le nom du serveur Exchange et les informations de version. Et si le compte réside dans une banque de remise, EnumerateAccounts affiche le nom de la banque de remise par défaut pour le compte.

EnumerateAccounts accède à la plupart de ces informations à partir de l’objet [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), hormis lorsque l’objet **Account** ne contient pas d’informations relatives au nom d’utilisateur et à l’adresse SMTP. Dans ce cas, EnumerateAccounts utilise les objets [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) et [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). 

EnumerateAccounts obtient l’objet **AddressEntry** en utilisant la propriété [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) de l’objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) obtenu à partir de la propriété [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)). EnumerateAccounts obtient l’objet **ExchangeUser** en utilisant la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) de l’objet **AddressEntry**. 

Voici l’algorithme qui permet d’obtenir des informations diverses à l’aide des objets Account, AddressEntry et ExchangeUser :

- Si l'objet **Account** contient des informations relatives au nom d'utilisateur et à l'adresse SMTP, utiliser l'objet **Account** pour afficher le nom du compte, le nom d'utilisateur et l'adresse SMTP, ainsi que les informations de version et le nom du serveur Exchange s'il s'agit d'un compte Exchange.

- Si l'objet **Account** ne contient pas d'informations relatives au nom d'utilisateur et à l'adresse SMTP, procéder comme suit :
    
  - Si le compte n'est pas un compte Exchange, utiliser l'objet **AddressEntry** pour afficher le nom d'utilisateur et l'adresse SMTP.
    
  - Si le compte est un compte Exchange, procéder comme suit :
        
    1.  Utiliser l'objet **Account** pour afficher le nom du compte, le nom du serveur Exchange et les informations sur la version Exchange.
        
    2.  Utilisez l’objet **ExchangeUser** pour afficher le nom d’utilisateur et l’adresse SMTP.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Comptes](accounts.md)

