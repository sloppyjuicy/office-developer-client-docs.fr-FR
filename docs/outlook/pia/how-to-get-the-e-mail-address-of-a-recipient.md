---
title: Obtention de l’adresse e-mail du destinataire
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5d145dadd974b6608da29cdf85a4624d6c452eb8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542575"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="1e289-102">Obtention de l’adresse e-mail du destinataire</span><span class="sxs-lookup"><span data-stu-id="1e289-102">Get the email address of a recipient</span></span>

<span data-ttu-id="1e289-103">Cet exemple montre comment obtenir l’adresse SMTP d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="1e289-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="1e289-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e289-104">Example</span></span>

<span data-ttu-id="1e289-105">Dans l’exemple de code suivant, la méthode GetSMTPAddressForRecipients prend un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) comme argument d’entrée, puis affiche l’adresse SMTP de chaque destinataire de cet élément de courrier.</span><span class="sxs-lookup"><span data-stu-id="1e289-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="1e289-106">La méthode récupère d’abord la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) qui représente l’ensemble des destinataires indiqués pour l’élément de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="1e289-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="1e289-107">Pour chaque [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) de cette collection **Recipients**, la méthode obtient ensuite l'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) qui correspond à cet objet **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="1e289-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="1e289-108">Enfin, la méthode utilise la [propriété PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) pour obtenir la valeur de la propriété http://schemas.microsoft.com/mapi/proptag/0x39FE001EMAPI, qui correspond à la propriété de l' **adresse\_\_** SMTP PR ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) du destinataire.</span><span class="sxs-lookup"><span data-stu-id="1e289-108">Finally, the method uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) property to get the value of the MAPI property http://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) property of the recipient.</span></span>

<span data-ttu-id="1e289-109">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1e289-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1e289-110">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="1e289-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1e289-111">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="1e289-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1e289-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e289-112">See also</span></span>

- [<span data-ttu-id="1e289-113">Destinataires</span><span class="sxs-lookup"><span data-stu-id="1e289-113">Recipients</span></span>](recipients.md)

